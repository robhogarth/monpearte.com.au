+++
date = "2019-04-29"
title = "You NEED Backups Tapes....Probably"
tags = ["Rant", "Backups"]
+++


As a veteran IT professional, I love to argue as much as the next veteran IT professional.  Mostly my arguments are harmless debates about the pros and cons of different brands of software, different architectural designs and who is the best companion in Doctor Who.

<!--more-->

!["It's Donna"](/images/donnanoble.jpg "It's Donna")

Somethings are a matter of opinion.  Apple VS Samsung?  Does your phone make calls? Yes, well, then it's down to whether you embrace the Church of Jobs or yearn for a change.

!["Instead of Church on Sundsays it's a Tuesday product launch"](/images/churchofjobs.jpg "Instead of Church on Sundsays it's a Tuesday product launch")

Sometimes in-depth (possibly heated) discussions are important when designing a system or preparing an upgrade.  Have all options been explored thoroughly?  Does the plan make sense? Has everyone affected been considered and consulted?

Many times, these "debates" could be called arguments, but usually at the end of the day everyone is striving for a better outcome and it's not personal.

It's said the currency of IT is respect.  And so, debates help to earn respect between peers.  All healthy stuff.  But don't think we don't argue about EVERYTHING.  I've been known to take a contra view just to be difficult.

However, I've found over the years one thing I don't argue about is backup tapes.

Even hearing the term backup tapes probably conjures up a number of different images in each person's mind.  Big reel-to-reel units from long ago.  Quarter Inch Cartridges from the later part of the last millennium.  Or maybe the modern LTO tapes.

!["Like it's always been, but better"](/images/ltotape.jpg "Like it's always been, but better")

One common phrase I hear is "Do people still use tapes?"  usually followed by "surely there's something better these days".  Well let's start by saying tapes are different in some ways these days, but fundamentally they are exactly the same technology that the industry has used for 50 years or more.  Start with a big roll of film type material, use a magnet and encode data onto it.  Start at the beginning and go until you've stopped or reached the end of the tape.

I like backup tapes.  I respect people who agree with me (but honestly who doesn't).  And while the media may seem primitive to today's ultrafast SSD type technologies, it has continued to improve over time at a rapid pace and has some distinct advantages over other storage mediums.

Firstly, how much can you store on a brand-new tape cartridge?  A Gigabyte?  Maybe even 1 Terabyte?

Wrong!  On a brand-new state of the art but totally not breaking the bank LTO8 drive you can back up a huge 12Tb of storage natively and compressed you can store up to 30Tb.

That's a lot of storage on a cartridge that's smaller than a VHS, and it can do it at 360MB/s.  Now that's not blindingly fast, but it's still respectable.  You'd have to have 10Gb interface to utilise the speed.

So what other advantages are there?  Well price for one thing cartridges are around $50-$100 each.  So much cheaper per Gb than SSD or HDD.  They are also physically resilient.  Drop a portable hard drive off a desk, and you'll be pretty worried about it.  Leave an LTO tape drive on the top of your car and drive off accidentally (totally not something anyone's ever done).  I'll pay good folding money that if you can find the tape, it will probably be ok.

But like a great 90s mid-morning TV sales person, there's more.  12TB not enough?  What about a tape library?  Like a regular old book library, but with shelves of tapes.  They start around 24 tape slots with one drive and can be as big as the floor of a building.  So 120TB no worries, just run 10 tapes automatically through a tape drive sequentially.

!["More is always better"](/images/ltotapelibrary.jpg "More is always better")

Too slow?  Ok add some more drives and run 10 tapes through 10 drives simultaneously.  Now you're getting 3.6GB/s.  That's some serious speed.
 "But I've got Veeam and I do backups plus replication.  I'm all set"
Well having disk to disk backups are great.  They are fast and easy, plus add on some replication and you've got the start of a great backup process.

But your backups are always online.  Which means if I'm on your system and trying to be malicious, I can potentially encrypt you onsite backups, your replication and then go through your file server and database and ransomware the lot.
Alternatively, that tape in the carpark that fell off a car, cannot be encrypted by a malicious hacker.  In fact, you can encrypt it yourself, so only you can read it later.

So, to recap, tapes are:

* Not as slow as you think
* Hold quite a respectable amount of storage
* Scale to massive capacity - libraries
* Completely offline - no ransomware
* Portable
* Resilient - can survive falls from car roofs (only at low speeds)

Any business needs to ensure it has great Data Retention, Business Continuity and Disaster Recovery plan.  If you don't have a comprehensive backup solution right now, I would strongly encourage you to have the conversation ask the scary question "What's the worst that could happen?".
In considering those possibilities I'd be surprised "why aren't we utilising tapes" is not a phrase that someone mentions.

!["This is the worst....it's bad"](/images/obliterate.jpg "This is the worst....it's bad")