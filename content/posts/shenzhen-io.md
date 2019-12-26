---
title: "Shenzhen I/O : Probably not what you expect to be an enjoyable experience"
date: "2019-12-26T11:24:00+02:00"
draft: false
cover: "/img/shenzhen-io/cover.png"
---


Games from [Zachtronics][zachtronics] has always struck a very fundamental chord
with me and it is the very thing that makes me who I am which I believe it is
the very basic fundamental nature of humans, seeking information in order to
satisfy their curiosity along with fueling their creative minds with ideas and
various concepts that would possibly enhance the whole world and everyone's
quality of living.

Or all of this is just me trying to justify the amount of hours wasted with
their games. It is known, however, that their games are known to be very nerdy
and very technical but somehow very well packaged, magically, in an entertaining
and enjoyable way. Well, at least for some people like me who are easily
intrigued by puzzles and similar challenges.

![Shenzhen I/O logo taken from the site][shenzhen-io-logo]

In this article, I will be talking about one of their titles called "[Shenzhen
I/O][shenzhen-io]" and this is perhaps my favorite title of them all. Shenzhen
I/O takes place, as the name implies, in Shenzhen, China where you work for a
small but stable embedded systems engineering house.

The game features a 46 pages manual in PDF available both in English and Chinese
and it is highly recommended that you take the effort to print the whole manual
and put it in a proper binder with tabbed dividers and also a couple of notebook
papers for "Engineering Notes" at the end. Other than that, it also features a
somewhat weird modern take of Assembly that you write for a particular series of
micro-controllers  and a "simple" CAD software where you place and connect
various components along with a simulator to test your design.

![The Assembly language reference which you will be using when writing code for
the series of fake micro-controllers used in the game.][shenzhen-io-manual]

Does this sound entertaining to you? Probably not. But for a lot of people who
are into "tech" games such as [Factorio][factorio] or a lot of [Minecraft mod
packs][mc-modpacks] such as [Tekkit][tekkit] which has most likely taken a lot
of your "extra" time to the point it is possible to classify them as secondary
jobs or maybe you're interested because of the theme of the game which features
a somewhat realistic "simulation" of a life as an embedded systems engineer but
have never taken the time to use that Arduino/Raspberry Pi kit you've bought or
maybe you're just too lazy to take classes in electrical engineering. Well,
whoever you're, you may be able to take a liking to this game.

Personally, I'm in both camps. Minecraft mod packs such as [Feed The Beast][ftb]
intrigues me because it challenges me to make a working infrastructure from the
ground up in order to ease the process towards an "end goal" which is either
determined by the game or by the player themselves and the nature of games being
inherently virtual made it really accessible for me to experience this challenge
without having to actually establish an actual factory in real life.

On the other hand, I've been interested in working with embedded systems for a
long time but I've never had the time nor money to pursue this interest. If I
have a brilliant idea that involves me making a DIY electronics solution to
solve it, I would immediately go to various classes and buy the stuff I need but
so far, I have none.

So, when a game like Shenzhen I/O features both camps and since it's a game
which makes the experience very accessible, I immediately put it on my wish list
and bought it on GOG when it was on sale.

So, How was it? I can safely say that this game has satisfied my itch of wanting
to try working with embedded systems. It was pretty amazing on how the game
could breakdown something that are complex in nature to a set of simple problems
along with in game lore which are progressed usually with emails that you
exchange with other co-workers along with a newsletter about life in Shenzhen.

Problems are usually presented with an email from a co-worker requiring a
working CAD design from you for a product. This product could range from a
simple fake CCTV camera and could be complex as a coin operated machine which
requires multiple components in order to handle coin counting and triggering the
device when a particular amount is inserted along with refunding the excess
amount.

Unlike other games where you're just presented with a set of problems and
passing one means you could pass onto the other one. Progressing in Shenzhen I/O
feels somewhat natural. The product have a backstory like you need to animate a
bunch of lights for a neon box which will be featured in an eSports event or
something odd like receiving contract work from a fully AI controlled
corporation. Among other "realistic" oddities such as hidden instructions or
features in your micro-controller which are only available in the chinese
version of the manual. For a game which main game play is writing assembly code,
it is really surprising how much lore there is.

![Example of a simple problem which involves creating a fake CCTV camera which
blinks a few LEDs in a certain pattern.][shenzhen-io-email]

You wouldn't believe how some issues that normally take you a couple of minutes
with a high level language (such as Python or C) while running on  a pretty
powerful system could possibly be when you're faced with a limited but powerful
version of Assembly and a very limited amount of read only memory and registers.

Since this is a game, a lot of technical "realistic" aspects are replaced with
something more accessible. For instance, you write code in the CAD software
within the micro-controller graphic itself. Which may sound weird but this is
the game's way to present the limit of how big your program could be. A line of
code taking up a space within the editor is more visible and much easier to
understand than an arbitrary value of a number. It is a very visual
representation of the issue.

Another example of this is the fact that your micro-controllers "need to sleep",
in this game, your micro-controller should sleep after it's done doing something
and could advance onto the next cycle. This makes it easier to understand what
your micro-controllers are doing since they're synced by "a sleep" and would
start on the next cycle together. You could also sleep for multiple cycles or
until you receive a packet from a bus which would also help with reducing power
usage.

There are also other things such as some of the components on your bin being
grayed out as "Not recommended", challenging you to think more creatively and
make good use of the limited resources. If that's not enough to tell how
terrible your design is, when your design passes the simulation which tests your
design on various scenarios, you'll be greeted by 3 charts which represents how
power efficient your design is among other things such as line of code and cost.

![A screenshot of the fake “Concept CAD” software being used to make a design
that solves the example problem above.][shenzhen-io-cad]

![The end screen of a problem which shows you the three metrics that indicates
how well your design is][shenzhen-io-verification]

This game is really amazing in terms of how well packaged it is. Problems are
presented as product ideas which has it's own backstory or specific requirements
that the client need and the very product idea is broken down into simple
bite-sized concepts.

To put in perspective, they're like those written math problems that you deal
with during math exams at grade school which you have to calculate the amount of
hamburgers Danny can fit within his tetrahedron container but unlike those,
they're presented really well and doesn't give the weird impression that written
math problems usually give.

The email conversation that you read while progressing the game doesn't feel
very robotic or forced. It has this natural feeling of "yet another day at
work", even though you barely speak or reply to them. The mailing list of life
in Shenzhen is a nice touch to present the cultural aspects which are going on
in this version of Shenzhen. Along with the 46 pages long manual which is
dripping with a lot of lore that would make sense when you progress the game
just represents how well crafted the whole game is.

In the midst of your journey, you will be given a chance to make the whole game
into a simulation toy that you could play around indefinitely and make a lot of
cool fake gadgets and even design test cases for them later on.

If you think to yourself that this game sounds interesting to you and you could
see yourself wasting your nights solving arbitrary problems for a fiction
company in China. Why not give it a shot? It's on [GOG][gog] and [Steam][steam]
for a pretty affordable price and it is not rare for it to be on sale. Not to
mention, GOG has a pretty good ["money back guarantee" refund
policy][gog-refund]. So, if you don't like it, you can just refund it easily.

Give it a shot and you can feel what it's like to be an embedded systems
engineer in Shenzhen, China and realizing how bad your designs were while also
having your head filled to the brim with various optimization ideas.

[zachtronics]: http://www.zachtronics.com/
[shenzhen-io]: http://www.zachtronics.com/shenzhen-io/
[mc-modpacks]: https://www.curseforge.com/minecraft/modpacks/tech
[factorio]: https://www.factorio.com/
[tekkit]: https://www.technicpack.net/modpack/tekkitmain.552547
[ftb]: https://www.curseforge.com/minecraft/modpacks/ftb-ultimate-reloaded
[gog]: https://www.gog.com/game/shenzhen_io
[steam]: https://store.steampowered.com/app/504210/SHENZHEN_IO/
[gog-refund]: https://support.gog.com/hc/en-us/articles/115000487189-GOG-COM-Money-Back-Guarantee-Policy?product=gog

[shenzhen-io-logo]: /img/shenzhen-io/logo.png
[shenzhen-io-manual]: /img/shenzhen-io/manual.png
[shenzhen-io-email]: /img/shenzhen-io/email.png
[shenzhen-io-cad]: /img/shenzhen-io/cad-software.png
[shenzhen-io-verification]: /img/shenzhen-io/verification.png
