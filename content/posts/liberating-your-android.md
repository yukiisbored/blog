---
title: "Liberating Your Android without having to sacrifice everything"
date: 2020-01-12T17:40:09+01:00
draft: false
count: true
toc: true
cover: /img/liberate-android/cover.jpg
---

> This article is a ***work-in-progress***. It is published in hopes to receive
> feedback in readability and writing improvements. Thank you for leaving
> feedback!

For whatever reason, you may decide to just ditch services from major internet
companies of the world and instead you go for services that are either hosted by
you yourself or by a tighly knit community of hackers building their utopia of
open and free software or maybe you just pay a company who will host the things
you need with a promise of them not taking a peek inside.

Whatever it is, you may find that you would like a peace of mind that is free
from algorithms trying to serve you personalised ads or prying your private
digital life.

You may find that the thing in your pocket as one of the biggest obstacle. The
device which has become the staple of the modern 21st century. The symbol of our
modern convenience. You may ask to yourself, "Is it really possible to liberate
and gain control while also not leave everything behind?". Leaving those apps
that you can't just live without them with reasons such as "I need it for work"
or "I use it to communicate with my friends and family". Well, why not?

# microG, the open source Google

microG is a project which aims to reimplement Google's proprietary services with
free software[^1]. Google's proprietary services has made itself to be a core
component of the Android ecosystem and thus, a huge obstacle in liberating your
Android phone.

A common example is push notifications, Google cloud messaging (GCM) provides a
central messaging API service which developers can use easily to send
notifications that will arrive instantly. This comes at a cost of their
application being tied towards Google's libraries and services but since most of
Android phones that are not in China has Google, a lot of them just go down that
route.

It would be really irritating to find that you're receiving any notifications on
your phone or even worse, your apps not work at all.

Thus because of services like GCM, Android has become known as the "not really
free" free software due to it's heavy reliance towards Google.

microG changes this by providing open source drop-in replacements which will
"emulate" the propriertary libraries and internal services and communicate to
Google with a free and open source codebase.

This helps a lot in your quest to liberate your phone while also not sacrificing
everything since you can still use most of your favorite daily non-free
applications while also taking steps towards breaking the shackles of vendor
lock in and "free" services.

Sound great, now how can I do it?

> By following the steps below, you **agree** that you will **take full
> responsibility** of your own actions. Liberating your phone may render your
> phone totally unusable and thus transformed into a paperweight. **I'm not
> responsible for any damages**.

This tutorial is meant to be read fully first before doing. This is not a
step-by-step tutorial where you will be guided and your hands held. You should
read the whole text and understand the possible scenarios that could happen to
your phone. You should do more research on your own. I'm simply telling you what
to look for.

# Liberating your phone

## Unlock the bootloader

The modern Android ecosystem relies on the bootloader as a safe guard to ensure
the legitimate state of the phone. This ensures that evil maid attacks cannot
happen to your phone while protecting the personal data and integrity of your
phone.

While this is good for the normal consumers, for us, it is one of the roadblocks
when liberating Android phones.

The method of unlocking varies between manufacturers. Phones from Good
manufacturers (such as Google or OnePlus) are unlockable with a simple command
of `fastboot oem unlock` after you ticked a box inside the developer options.
Some manufacturers require you to login to their website and put some
information from your phone in order to get the key and it's just a `fastboot
oem unlock UNLOCK_KEY` away.

However, some terrible manufacturers will make you wait for an arbitrary amount
of time that could range from a week to 3 months or even worse, not giving you
the ability to unlock at all.

Whatever the case it is, you could find a way to do it by going to the XDA
Developers forums and search for your device. There'll be most likely threads
that will show you how to unlock the bootloader or threads that will tell you
that it is not possible because the manufacturer doesn't give a shit.

## Get LineageOS on your phone

LineageOS is simply a free and open source distribution of Android. You can
think of it as something like a Linux distribution which prepackages Android
into a usable state. LineageOS also makes and maintains basic applications which
are taken away from Android Open Source Project such as a web browser, a phone
dialer, a camera application, etc.

There are two version of LineageOS, Official and Unofficial.

Official builds of LineageOS are maintained by the LineageOS team themselves.
They will ensure compatibility with your phone for some amount of time.

Unofficial builds are maintained by a simple member of the community that just
want to have LineageOS. It should be noted that unofficial builds vary by
quality a lot. Some may bloat their build with unnecessary apps or unwanted
features. However, there are some that will take care of their build and treat
it like official ones by giving it the whole treatment with OTA update and
regular security updates.

For official builds, you can simply go to https://download.lineageos.org/ and
find your device. If your device isn't there, you can go to the XDA developers
forum and find your device.

If you're not familiar with how to flash your phone, once again, you can go to
the XDA developers forum and find your device. For most devices, it is the same
4 steps: Flash TWRP, Wipe data, Flash LineageOS, Reboot. However, for some
phones, it may be difficult and require a bit of work. This is true for a lot of
phones that are using the new A/B partition scheme.

### Whoops, I bricked my phone!

Not to worry, Android comes with fastboot/bootloader mode which will allow you
to restore your phone. Some phones will automatically boot in case of failures
into what's called EDL (Emergency download mode).

You can easily find the firmware images along with instructions by going to the
manufacturer site. If you couldn't find it, just go to XDA and find your phone.
There are most likely people who have dumped images or simply mirror them from
the manufacturer website along with instructions.

From my experience, I have never had any fully hard bricked phones. All of them
are always easily restorable with software. The only worse case scenario that I
had experienced is having to upload fresh vanilla firmware with fastboot which
is trivial.

## Install microG

microG relies on Signature spoofing in order to "fake" being a legit Google
application. Some distribution of Android support this natively but LineageOS
doesn't do it due to the fact it being a high security risk.

In this tutorial, we're going to use a distribution of microG called NanoDroid
which eases setting up microG. NanoDroid is also capable of adding this
"Signature Spoofing" feature to your OS, if it is supported. If not, no worries,
there's an alternative method.

NanoDroid also includes other quality of life features such as a drop-in open
source Google Play Store replacement where you can download your normal
proprietary apps and also F-Droid along with the privileged extension.

### Install Magisk

Magisk calls itself a "Systemless interface". What that means is Magisk gives
you the possibility of modifying the system files on your phone without making
any permanent changes.

This helps in modifying your phone without having to fully commit to the
changes.

You can download Magisk from the official XDA thread:
https://forum.xda-developers.com/apps/magisk

You need both the flashable zip file along with the APK for Magisk Manager.

Do not download Magisk from any other site since they're most likely scams
littered with viruses.

The installation process is simple:

1. Go to recovery mode (most likely to be TWRP).
2. Install the flashable zip file.
3. Reboot to the OS.
4. Install the Magisk manager.
5. Done.

### Install NanoDroid

You can download NanoDroid from the official website:
https://nanolx.org/nanolx/nanodroid

You need the NanoDroid zip file along with the setupwizard zip file.

The NanoDroid zip file is huge because it also contains other stuff such as
other Free software along with some random stuff such as Nintendo font / Zelda
ringtone.

You may not want all of it and only care about getting microG, F-Droid along
with the play store replacement.

This is where the setup wizard comes in. The setup wizard allows you to choose
what you want to install.

The installation process is as below:

1. Go to recovery mode.
2. Install the setupwizard zip file.
3. Choose the configuration location. I usually choose external_sd since I
   always have external storage on my phone where I place all of my recovery zip
   files.
4. Choose the stuff you need. If you want to go full minimal, you can choose the
   following:
   1. In the generic setup page, select **only**: Maps API v1 and (maybe) Init Scripts.
   2. In the microG page, select Full.
   3. In the F-Droid page, select Official.
   4. In the NlpBackends[^2] page, choose Ichnaea and Radiocell. You could choose
      whatever you're comfortable with.
   5. In the Google App Store page, choose Aurora + FakeStore[^3].
   6. In the App Setup page, You can either choose none of it or just leave it
      since it won't be honored anyway.
   7. In the Debloat Setup page, it's the same deal as the App setup page.
5. Install the NanoDroid zip file.
6. Reboot.

### Verify microG is working

After your first boot up with NanoDroid installed, you need to verify that
everything is working.

You can do this by opening the "microG settings" app which is now installed (and
replaces the Google settings that you normally find).

For the first time, it may ask to be granted permissions. You can press it and
grant it all of the permissions it need.

From there, you can go to "Self-check" and verify that everything is working.

If "System spoofs signature" is ticked (along with others), congratulations,
you've installed microG.

If not, it's not the end of the world as I present you the alternative method of
getting signature spoofing to work.

### When signature spoofing fails

#### Install EdXposed

Xposed framework is a framework/library which allows applications to modify
applications without having to change the code of the application directly.
Instead, it does this by hooking to the function of the application. From there,
you can change it's behaviour. This could range from theming a particular app to
various quality of life improvements.

We're going to use a more maintained version of Xposed called EdXposed which
supports modern version of Android with it we can modify the system to support
signature spoofing.

The project is hosted at GitHub on: https://github.com/ElderDrivers/EdXposed

The install process is simple with Magisk:

1. Open Magisk Manager.
2. Go to "Downloads".
3. Search for "Riru - Core" and Install.
4. Reboot.
5. Open Magisk Manager and Go to "Downloads".
6. Search for "Riru - EdXposed" and Install.
   * You may notice there are two version of it. Simply try one of them. If it
     doesn't work, you can try the other one.
7. Reboot.

After that's done, you need to install the companion app.

The companion app is available on GitHub: https://github.com/ElderDrivers/EdXposedManager

To download a build of it, you go to "Releases"[^4] and download the latest
version.

After you've downloaded it, just install it and verify that EdXposed is running.

#### Install FakeGApps module

We're going to use an Xposed module called FakeGApps which will add the ability
of signature spoofing.

The project is available at https://github.com/thermatk/FakeGApps

The install process is simple with EdXposed:

1. Open EdXposed Manager.
2. Go to "Downloads".
3. Search for "FakeGApps" and Install.
4. Go to "Modules".
5. Enable FakeGApps and reboot.

After all of that is done, you can verify that signature spoofing is working by
doing the microG self-test again.

Congratulations, you have a phone free from the shackles of proprietary
services. Now, it's time to install all of those apps you need/want.

# Questions?

Need any help? You can contact me

* Email: hi (keong[^5]) yukiisbo.red
* Fediverse: https://bsd.network/@yuki_is_bored
* More contact info at https://yukiisbo.red

I'll add the commonly asked here.

[^1]: The obligatory "Free as in freedom, not free beer"
[^2]: NLP backends provides Network based location. This is the service which
      will determine your location with the surrounding Wi-Fi network and cell towers.
[^3]: FakeStore is part of the microG which will lie the existence of the Google
      Play Store. Helpful for those pesky applications which won't work.
[^4]: You need to open the GitHub page on a computer or in desktop mode to see
      this option.
[^5]: Keong means snail in Indonesian. You know which symbol I'm talking about, right?
