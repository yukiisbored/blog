---
title: "My Minecraft days"
date: 2019-04-29T23:06:23+02:00
draft: false
---

I used to go under different pseudonyms, one of which is "captainFroster". I
used "captainFroster" during my younger days where Minecraft was in its peak
popularity and I was known for ... *Minecraft*. I had a Minecraft server called
Project-Z¹ or Nucleus Servers. You may not heard of it and I'm not surprised since
it was targeted towards Indonesians. It was my spin on the hardcore survival
genre. This was at the time where zombie survival games like DayZ was popular
racking thousands of online players. I wanted something like DayZ but less focus
on the action rather focus on the extreme survival experience and community
building.

Project-Z was focused on giving an extreme survival experience by being in a
world where zombies roam the world freely. Unlike most Indonesian servers which
mostly consists of random elements, Project-Z had a clear running theme and
a target. I have experience with the Java programming language so I was able to
write Bukkit plugins in order to achieve it. Back then, I didn't have a lot of
programming experience. So, With the help of a friend called Steve, We wrote the
plugins for it.

The zombie survival experience part was easy. We found this plugin called
Apocalyptic on Bukkit plugins but It was largely unmaintained and had some bugs.
I forked it and made the fixes required to make it work with newer versions of
Bukkit. The hard part? Balancing. Balancing is one of those problems that have
no end in sight. How do we make the gameplay balanced? How do we make it fair?
How do we even know it's fair?

Balancing isn't only about tweaking damage multipliers. It can also be other
game elements such as spawn points, world area limit, economy, etc. In a complex
game like this one, it's hard.

How we did the balancing on the game economy was an interesting approach that we
took. Instead of doing it the old way and have a centralized shop. Why not make
a real working economy? One of Project-Z's points is it's focus into community
and community building. Factions are first-class citizens and have the upmost
importance. So, why not have an economy where they can do actual trade? Like
trading items, land, etc.

So this is how we did it, we defined a fixed price for a single item. We used gold
because it had the good rarity ratio in comparison to other materials in the
game. We fixed it to 30 bucks for one piece of gold and wrote a plugin which
tracks the pricing of items based on transactions that are done by players. With
this, players define the price rather than the admins.

Okay, this fixed the issue for normal item pricing. What about custom items like
guns? For that, we made crates. Yes, crates or loot boxes as people call it
nowadays. However with this one, we didn't actually take real money, We never wanted to
have real money to give an advantage in the game. Crates are there just to
randomize the value of each guns based on availability and demand. We also added
Airdrops into the game so people who don't have money or ~~sadistic~~
adventurers can find supplies of ammos or get weapons.

We also have other balancing elements such as random spawn on first join,
ranks, land limiting, etc.

What about making the experience more mobile and fun? We added machines.
Machines such as drills, automated farms, airships, boats, cars were possible in
our server. I believed it unlocked more fun and mobility into the zombie
survival experience and the faction raiding.

People can build airships which deploys nukes to enemies territory, automate
boring manual labor such as mining, farming, inventory sorting easily. With
this, you don't need a lot of people to survive. Having good automation
infrastructure at bay also helps survival.

With all of that, I believe we had created one of the best Minecraft servers
(at least in Indonesia) and I really love playing it myself. To this day, I
still have fond memories of building my faction, raiding people, being a dick to
other players, etc. It was a fun sandbox zombie survival experience.

It was popular for an amount of time but ended up loosing players since
Minecraft was slowly becoming a game for kids who don't like dedicating their
time. These people prefer having a more spoiled gameplay with not dropping
inventory on death, op donation perks, etc. While our server which focus on
excellent gameplay don't get a lot of attraction. Our donation perks are only
cosmetics.

In the end, It died because I cannot afford to run it anymore and my parents
were pissed at me about focusing on it rather than my studies.

Not to mention the 1.9 update made PVP less fun and make it more annoying. Damn
you, Microsoft.

So, I released our plugin code as GPLv3 and that was it.

A lot of people see it as a waste of time. They see it as a waste of time of
writing code for a video game rather than something useful. Well, I don't.

Running this server taught me many things. It taught me game design and how to
achieve a balanced experience. It taught me a lot about programming. In the
beginning, I'm not too familiar with OOP concepts such as Polymorphism among
other things but in the end, I'm fluent in Java. I learned about reflections,
runtime patching, mix-ins in Java, etc.

All of that plus finding my one true love: Managing servers.

Running a Minecraft server taught me the system administrator mindset. Other
people just run it inside a simple tmux/screen session. Me? I ran it inside a
docker container so I can have full control of the resource that was being

I learned iptables, writing init scripts, security mitigations, etc.

You can say that from that experience of running a Minecraft server that I
became the system engineer that I am today and yeah, it helped me a lot.

Thanks to my experience in Docker and my point de vue of being a proficient
system engineer, I'm able to win Google Code-in by introducing concepts such as
CI/CD, reproducibility, linting, etc to projects such as Loklak where I migrated
it over to Gradle from Ant while keeping Ant users happy.

Today however, I still mourn of not having an experience like it. Maybe I'll
create a plugin pack for Cuberite or a full fledged game? Well, I don't know and
I can't guarantee anything. I just miss it and the hours of fun it gave me.

EVE Online gives me almost the same fun and satisfaction as my old server but I
want something that has more action and less space-y. Back to RimWorld / Dwarf
Fortress, I guess.

Anyway, that's all for today. Feel free to cringe at [my old code][1].

¹: Yes, I know there's a porn site called "Project-Z". Just ignore that.

[1]: https://gitlab.com/nucleus-servers/NuPlugins
