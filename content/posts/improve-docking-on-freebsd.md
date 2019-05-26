---
title: Improve Docking on FreeBSD
date: 2019-05-26T16:23:33+02:00
draft: false
---

*a.k.a Yuki's first baby steps to FreeBSD development*.

I love my Thinkpad X220 and the Ultrabase docking station just makes it more
awesome. I mean like all of my ports (DisplayPort, Keyboard, Mouse, Ethernet,
Audio, etc) is already connected to this convenient dock and all I have to do is
slap my X220 to it. That really makes the experience a lot better since I'm
currently a student and I sometimes have to bring my laptop to school. Since my
laptop is also my only machine, I use it as my primary daily driver until I have
my own PC.

On Windows, when I dock my machine, it automatically switches the monitor as per
my configuration and also changes the audio device.

Meanwhile, on FreeBSD, nothing happens. Well, some stuff do happen in the
background but it doesn't switch monitor nor the audio device.

Practically, what FreeBSD does is only change the value of `dev.acpi_dock.0.status`
from `0` to `1`[^1].

Okay, so, what can we do with this limitation?

We can always have a while loop that checks `dev.acpi_dock.0.status`
indefinitely. Well, while it works, I dislike it personally.

Since FreeBSD 5.0, FreeBSD have this fancy tool called `devd(8)` where we can
run userland programs when kernel events happen. Like enable a bluetooth USB dongle
when it's plugged in, download a firmware when a device is plugged in, switch
keyboard devices for the console, etc. It is the equivalent of udev in Linux
land just a lot *saner*[^2].

So, why don't we take advantage of this new tool and just have a cleaner
solution overall. I mean Linux does it (with the event-based infrastructure
provided by `systemd` and its ~~enslaved~~ sub-projects).

After googling around for solutions, I stumbled upon the following email thread
on freebsd-mobile: [acpi_dock and devd question][email thread]. In that thread,
`iwasaki@` wrote a diff that add a notify call to tell `devd(8)` when we're
docked and undocked. Well, the diff kinda works as-is but we need to make some
changes to make it work with today's version and add a check to see if `devd(8)`
is even running or not. So, I made it those changes and it works.

I tried contacting `iwasaki@` if he wants to get the patch submitted himself but
I didn't receive a respond so I just submit it along with my changes myself on
FreeBSD's bugzilla[^3]. You can go to
[my personal freebsd-wip repository][freebsd-wip] on GitLab and see
[the patch][commit] applied on my laptop's working branch.

Now, we got the kernel and `devd(8)` stuff done. We can easily add the following
to the `devd(8)` configuration (`/etc/devd.conf`):

```nginx
notify 10 {
       match "system" "ACPI";
       match "subsystem" "Dock";

       action "/etc/acpi_dock $notify";
};
```

That snippet will make `devd(8)` run `/etc/acpi_dock` with the first argument as
the dock status. The status will return `0x00` when we're undocked and `0x01`
when we're docked. Simple.

With this we can do the stuff we want. Just write a simple script that will do
what we want et voilà! Well, no, not really.

While we can change audio devices without needing to be inside an X server, we
can't switch the monitor, restart the window manager and bar, etc. To do that we
have the following choices:

1. A very hacky `su` and `DISPLAY=:0` solution which will change the monitor and
   everything else
2. A daemon running inside the X session which will listen to a simple trigger
   and run the needed scripts within X.

I've chosen the second one mostly because it's a lot cleaner in the long run,
less edge cases to think about and just better design in general. While, the
hacky method might work, I couldn't get it to work for switching the monitor.

Okay, so I made a program called `dock-trigger(1)`. It's a simple POSIX sh script
that listens to the `SIGUSR1` signal and runs scripts depending on the dock
status. You can see the program in my
[personal dotfiles repository][dock-trigger].

For the `/etc/acpi_dock` script, I just have it check the PID files which is
placed by `dock-trigger(1)` and send the `SIGUSR1` signal to the procceses.

```sh
#!/bin/sh

for pid_file in /tmp/dock-trigger_*.pid
do
    /bin/kill -USR1 "$(cat $pid_file)"
done
```

With `dock-trigger(1)`, I can write scripts on
`~/.config/dock-trigger/docked.sh` and `~/.config/dock-trigger/undocked.sh`
which will run when my machine is docked or undocked respectively. Awesome.

My `undocked.sh` script is simple. All it has to do is switch the audio device
from the external monitor to the internal speakers, switch from the external
monitor to the internal one and restart the window manager along with the bar.

```sh
#!/bin/sh

sysctl hw.snd.default_unit=0

xrandr --output LVDS-1 --auto \
       --output DP-2 --off

bspc wm --restart
pkill -USR1 polybar
```

Now, for my `docked.sh` script. It basically does the same thing as my
`undocked.sh` script but in reverse (switch the audio device from internal
speaker to the monitor, etc).

```sh
#!/bin/sh

sysctl hw.snd.default_unit=2

while true
do
    if xrandr | grep "DP-2 connected"
    then
        xrandr --output LVDS-1 --off \
               --output DP-2 --auto

        bspc wm --restart
        pkill -USR1 polybar

        break
    fi
done
```

Okay, I have to put it inside a while loop for the monitor change because it
takes a while for `intel(4)` to attach the external monitor and get X to
recognize it. Oh well.

With everything, it works really well though I'm currently encountering some
issues because of how bspwm handles monitors.

`bspwm` really doesn't react to monitor change really well. It doesn't rearrange
the windows at all. Is it a `bspwm` bug? Well, I don't know. How `bspwm` handles
multi monitor is already weird itself so whatever. I'll figure out something
later but for now, it works nicely and I can just dock/undock my laptop and
everything will work :).

[^1]: Well no, it also does some other things like attaching and detaching device and all of the ACPI goodness.
[^2]: What kind of grass were they smoking when creating the
      [rules syntax][udev rules]!?
[^3]: [FreeBSD patch submission](https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=238138.)

[email thread]: https://marc.info/?l=freebsd-mobile&m=120186653700412&w=2
[udev rules]: http://www.reactivated.net/writing_udev_rules.html#syntax
[dock-trigger]: https://gitlab.com/yuki_is_bored/dot/blob/master/x/.local/bin/dock-trigger
[freebsd-wip]: https://gitlab.com/yuki_is_bored/freebsd-wip
[commit]: https://gitlab.com/yuki_is_bored/freebsd-wip/commit/54fa798f573dfe0ddcf6c8a38c3969d341d230a1
