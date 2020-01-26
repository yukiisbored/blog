---
title: "Trying to live without Google (Part 1: Email)"
date: 2020-01-25T21:44:48+01:00
draft: false
cover: /img/free-google-pt1/cover.png
---

For the couple of years or so, I've decided to start living without being
dependant on the electronic giant that is Google. Is it actually possible? If
so, how hard is it?. Well, it's been a wild ride.

# Why do you want to leave Google?

It's probably the first question that I get a lot when doing this project. Why
do you want to leave Google services? They're such a conveience and you could
probably say they're somewhat essential to our modern day style of living. Hell,
it is essentially a verb in almost every human languages.

Google has become something so embedded within our life. Why do you want to
leave it?

Really the main reason for me is just simple curiosity. As a geek with system
administration as a profession, is it difficult to escape centralized services
from big internet companies? I'm also quite curious about the alternatives which
are often paid or run by volunteers and want to compare the experience with the
free services that are run by Google.

There are however other reasons to do something like this, however they vary a
lot depending on your personal views on the company and others like it.

The biggest common reason is privacy. It is known that big internet companies
collect massive data about you so they can serve you with advertisements in
order to serve you with their services. While for some people find it okay
because they're typically fed to "robots" or "AIs" and see it as a necessary
"evil", some people are skeptical as scandals and cases of data abuse from big
internet companies often arise almost every day. From the big infamous scandal
of Facebook with Cambridge Analytica[^3] to Google obtaining data of millions of
patients in the US without their expressed consent[^4]. It is understandble why
it's hard for them to trust big companies such as Google, Amazon, Facebook and
others.

However, there are other reasons such as not wanting to support the big internet
monopolies. Services that are offered by the major internet companies are
somewhat in a very monopolistic position as they can do whatever they want and
since there's no good alternatives, they'll stay. This is very evident with how
YouTube treats it's creators with things such as giving music companies the
ability to issue baseless copyright claims, demonitizing channels without any
specific reason and even silencing them.

I firmly believe any type of "monoculturalism" is bad. Embracing monoculturalism
develops into the heavy dependance on to the one thing and once that thing
collapse, everyone is affected. Having your whole existence reliant upon one
thing is bad. If you only rely on Facebook to do your business, well, your
business will collapse if Facebook suddenly goes under. You have to diversify.

I saw my reliance on Google's reliance as a "vendor lock-in" and in my opinion,
that is bad. So, how can I get out?

# First step, Moving out of Gmail

Changing email wasn't hard for me as I wasn't the avid email user. So signing up
to another email provider isn't a huge concern for me. So, I started looking and
trying out different providers. These are the ones that I've tested or have
experience in the past.

There paid email providers such as :

* [Fastmail][fastmail-website] (2 GB for $ 3 / month)
* [Mailbox.org][mailbox-website] (2 GB for € 1 / month)
* [Kolab Now][kolabnow-website] (2 GB for CHF 8.99 / month)

There are also companies / organizations who offer it for free :

* [ProtonMail][protonmail-website] (500 MB)
* [Disroot][disroot-website] (1 GB)

## Experience with ProtonMail

The first one that I tried was ProtonMail. This was during the time when
ProtonMail was relatively new and I was lucky enough to get a pretty nice email
address, yukinagato@protonmail.com[^5]. The web client was really nice, probably one
of the best even. However, I have some issues with it.

My main issue with ProtonMail was the fact I couldn't use the typical email
stuff such as IMAP/SMTP. This was somewhat of a dealbreaker for me as I want to
use my clients such as Thunderbird or GNU Emacs. This was during the time where
ProtonMail Bridge wasn't a thing and even if it is a thing, it still means I
need a special application that isn't going to be available everywhere.

There are other concerns however such as the fact the server code isn't really
open source, only the web client. While you can verify the client code and just
assume everything is all good and dandy. How are you supposed to know that they
will keep their promise? During these times, there were number of speculations
around ProtonMail[^6].

Another deal breaker is not being able to use your own GnuPG keys. If I want to
send an encrypted email to someone that doesn't use ProtonMail, how am I
supposed to do it? ProtonMail does use GnuPG as their encryption backend but
you have to use their platform to do so.

I've come to the conclusion that I don't really care about server-side
encryption at all. If I really want to send something in secret, I would use a
highly accepted standard that is GnuPG/PGP and it's way safer to do that
locally. While ProtonMail's end-to-end encryption to other ProtonMail users is
cool and all, the fact that I have to use their platform is a major dealbreaker.
Instead, I would prefer using standard protocols that everyone can use.

## Disroot, the community built empire

Disroot is a community project maintained by volunteers and depends on support
of it's own community. Disroot provides users with access towards free online
services such as Email, XMPP, Cloud and many others. They're built with open
source software.

My experience with Disroot was really good. Their Raindrop client is really nice
along with Nextcloud which is a really nice bonus. In fact, I would say if
you're looking for something that is high quality and free, Disroot is your best
bet.

It's passionately built by a team of volunteers that really care and use it as
their main method of communication. The overall hacker culture is there and I
like it. Disroot is built with the philosophy of using decentralized services,
user privacy and total transparency. It is common to hear on the development of
the project.

However, there's one issue. I started to use email more and the limited space of
1 GB is starting to become a huge limit for me. This was also during the time I
was starting to plan my future as high school was ending soon. Another thing is
i'm somewhat stuck with my pseudo that is `yuki_is_bored` as I legitemately have
actual certificates under that name along with my entire existence on the
Internet is connected to it and having to explain from someone who works as a
recruiter or work at an embassy of a foreign country why your email has "Yuki is
bored" is hard. They are not familiar with hacker/internet culture so it's hard
to explain it in the boring professional language that they could understand[^8].

So, I started to care about my "professional" image with stuff like having my own
domain[^7] among other things. As far as I remember, Disroot does have an option
to use your own domain as long as your donate but if I'm paying for something, I
might as well compare it to others.

## Brief experience with Kolab Now

At first, I thought of Kolab Now as it is oftenly mentioned as one of the best
providers that uses open source software. Being curious, I decided to try it.
Seeing the prices and the many options, I ended up with a somewhat expensive
price of around $ 15 / month (if I remembered correctly) with everything I need
and it has 30 days money back guarantee. So, I decided to at least try it.

The experience wasn't really smooth sailing. Since I wanna to use my domain, I
spent a lot of time hunting for the option until I realize that I need the
groupware account to do so and it is very expensive. The web client wasn't good
either. It used Roundcube which was not a decent experience. The overall
experience was somewhat mixed and I wasn't a big fan of it.

So I've decided to just request a refund and close my account. The support
people was nice and I left some feedback.

It should be noted that this was probably around 2-3 years ago and things have
changed a lot. Looking at their website now, it looks a lot cleaner than their
old one and the screenshots resembles a much better interface than the old one.
However, it is still the premium option when it comes to email providers.

If you're looking for something that you want to use for your organization or
company, Kolab Now is a really good choice. It is also understandable that Kolab
Now is probably one of the only few choices that offers as many services while
located in Switzerland which is home to very strong data privacy laws.

## Moving onto FastMail

While looking for other options, I stumbled upon FastMail. I'm not sure what
brought me to it but the prices are really decent. 30 GB for $ 5 / month? Hell
yeah!

It also have some technology called jmap which a new "standard" pioneered by
FastMail which offers a better mobile experience.

FastMail has everything I needed and with a really nice web interface on top of
that! Integrating with my domain is easy and it also comes with a bonus of cloud
storage and I was happy for a while.

And then stuff happened, Australia was doing crazy shit regarding encryption and
data privacy. FastMail is based in Australia so I was somewhat concerned. The
other thing is that I wanted more. The cloud storage as a bonus was nice and all
but it has some limitations such as a file has a size limit among with other
annoyances when syncing stuff[^9].

During this time I was in language school and had to use their local computers
from time to time, so I wanted something that also have some office suite stuff
where I can have the whole Google-like experience. A friend of mine mentioned
mailbox.org which have cheaper prices and is based in Germany. The fact that
they use open source software is really hooked me in and as a nerd who's never
satisfied with anything, I decided to hop over to mailbox.org.

## Hoping over to mailbox.org

During this time, Email was becoming a very important factor of my life so
migrating wasn't as easy as before. However, it has become easier since I use my
own domain name so I don't have to manually change addresses. I still have to
migrate a bunch of my emails, so how am I supposed to do that.

I could use OfflineIMAP and just do it from there but during this time, I was
living in a student dorm where internet access was limited to my mobile data.
Mailbox.org have the option of migrating emails with a third-party service
called Audriga and offer a € 3 voucher. With Audriga, migrating my massive
amount of email was a snap. I really recommend it to people who just want an
easy and fast way to migrate their massive amount of email.

OX, the platform which Mailbox.org uses, is really nice. It has a pretty good
interface, not as snappy as FastMail/ProtonMail but very usable nonetheless, not
bad for open source software. Getting things working such as desktop/mobile
integration is easy thanks to OX's somewhat rich ecosystem. On Windows, I could
easily setup OX Sync to be able to access my cloud drive. On Mobile, I could use
the OX suite of applications to access email, drive, tasks, calendar, contacts.
It's overall a really nice all-in-one solution for those who want something
resembles Google's services but powered by open source software, independent
and doesn't spy on you.

There are a couple of criticism that I have however. When using 2FA, you have
two choices: not allowing applications (such as IMAP/SMTP) to access your
account and only use the web client or use your normal password when using
applications. This is because mailbox.org has an odd way of doing
authentication. 2FA basically means your password is now the OTP token[^1] plus
a secret code which is a good security measure to ensure that your account isn't
reliant on a static fixed password as a protection (kinda like Yandex with
Yandex.Key) but rather a dynamic always changing password where the only weak
point is the secret key which you only exchange once.

This is good and all until you notice that Mailbox.org doesn't have a feature
which everyone else have that is App Passwords. A randomly generated password
that is designated towards a specific application. This would mean when one of
your app passwords is compromised, it doesn't mean the end of the world. You
could easily just revoke it and make a new one. This is a really awesome
security measure since now you can have 2FA enabled and only issue app passwords
each to your applications.

Sadly, Mailbox.org doesn't support this due to how they do authentication with
LDAP. However, I do believe this is an arbitrary issue that is made by humans,
not something that is physically impossible.

The other thing about how weird mailbox.org 2FA is the fact that the secret code
is only 4 digits long. Some people may view this as okay, however there are
other people that just want to use their password and then the OTP code at the
end. And also the lack of support with U2F/WebAuth keys is pretty annoying.

The other criticism that I have is mostly towards OX's office suite, why does it
use Microsoft's propriertary format by default instead of the Open Document
Format? I find it somewhat weird. I can understand that support for Microsoft's
format is important for business/enterprise users but I don't think that it
should be the thing supported by default. At least give me an option to save as
ODF.

The Open Document format intercompatibility support between OX Office Suite and
LibreOffice is somewhat mixed. Sometimes it's really well but other times it's
really poor to the point the encoding is changed to Latin-1 and I end up with
weird symbols when writing in French.

However, it is still a decent usable service and it's probably the best
contender for a good all-in-one Google replacement package.

## Wrapping up different email providers

Unlike others, Email is quite easy to hop out of since it is still built with
open and recognized standards that are widely used and I doubt Gmail will
replace the whole Internet email infrastructure in the near future[^2].

There are many different types of email providers that offers different things.
They typically target certain niche. However, to conclude from my previous
experiences:

1. If you just want an **encrypted email provider** who utilizes **server-side
   encryption** at a cost of **locked in to their platform**, just use
   [ProtonMail][protonmail-website].
2. If you want something **free** that uses **open standards** and **open source
   software**, use [Disroot][disroot-website].
3. If you want to don't mind **paying for just email**, use
   [FastMail][fastmail-website].
4. If you want a **good collaborative environement for your organization/company**
   that is powered by **open source software** and hosted in **Switzerland** where data
   privacy is king, use [Kolab
   Now][kolabnow-website].
5. If you want a good **drop-in replacement** for **Gmail**, **Google Docs**,
   **Google Calendar**, **Google Drive**, **Google Contacts** with a pretty
   decent pricing and to top it all of uses **Open X-change, an open source
   cloud office suite**, use [Mailbox.org][mailbox-website].

# To be continued...

As I'm writing this article, I noticed that I don't want to write it for too
long. Having a long article is hard to maintain and nobody wants to read a
really long one. So I decided to make this into a series about quitting Google
(and services from other big internet companies).

Next time, we'll talk about Fediverse and other decentralized services.

[^1]: The ones that you typically associate with "Google Authenticator" which
      generates a 6 digit token every couple of seconds or so.
[^2]: There's still the possibility since almost everyone uses Gmail.
[^3]:
    https://en.wikipedia.org/wiki/Facebook–Cambridge_Analytica_data_scandal
[^4]:
    https://www.wsj.com/articles/google-s-secret-project-nightingale-gathers-personal-health-data-on-millions-of-americans-11573496790
[^5]: Don't bother sending any emails to this one as I don't use it anymore.
[^6]: https://news.ycombinator.com/item?id=18101090
[^7]: Which is a nice touch for me since at the time, I wanted a career around
      system administration or operations. So having my email on my own domain
      is a nice "I know how to do shit".
[^8]: It is still not a legit excuse to my shitty online pseudonym. Please
      choose yours wisely and just don't make one with the goal of pissing a
      couple of close friends on IRC.
[^9]: Getting CalDav and CardDav working nicely wasn't pretty and it lacked
      support for tasks.

[fastmail-website]: https://www.fastmail.com/
[mailbox-website]: https://www.mailbox.org/
[kolabnow-website]: https://kolabnow.com/
[protonmail-website]: https://protonmail.com/
[disroot-website]: https://disroot.org/
