+++
date = "2019-02-10"
title = "Software developers pick up your game!"
tags = ["Rant", "Software"]
+++

For too long IT teams have struggled with poor software.  It's time for software developers to pick up there game
<!--more--> 

Sysadmins are busy people. We have passwords to reset, backups to check, project stand up meetings to sit through etc.  Occasionally we may even log into a server.
If we do things right, we can maintain the delicate balance to ensure things keep running, tickets are completed and Karen from accounting gets that file back she swears she never deleted it just "vanished".

One thing you can always count on being problematic is custom software.  Microsoft Office works fine, your SAP system costs the same as a GDP of a small African nation but it gets the job done, but every department has that one application they use to get things done.  You know the one.  It's vaguely common enough in its specific industry, but it's not big enough that if you google it errors you get any kind of response.

Why do IT people hate these apps?  Because they are terrible!

<!--more-->

Sure, your colleagues that use it love the app.  It gets the job done as far as they are concerned.  But when you look at it you can see it for what it is.

Frankly I've had enough of them.  Today I'm calling you out!

I've worked with hundreds of these apps and I guarantee they take up far more time than they should.  They are asset management tracking, custom project management etc and they come with a price tag that could fund all of IT's budget for 5 years.

!["Yes that is a lot of zeros"](/images/sapcost.jpg "Yes that is a lot of zeros")

Let me break it down.  Warning this may be a trigger warning for some IT greybeards.

Poor install procedure
---
After getting sign off for a shiny application management system like SCCM, you start the sort of tedious but ultimately rewarding job of setting up your applications to  install automatically inside your system.  Your standard apps take 2mins each.  You even get some tricky little fixes in there to make your desktop environment fully self-service, compliant and consistent.

But you start through the custom apps and the troubles start.  No MSI package...hmm no problem, an EXE with some command line arguments and a switch to make it all silent and you'll be laughing.  Notepad++ works like that.

You run the app with a /?, and no help text.  You read the manual...nothing mentioned.  You attempt to find something online...0 results found.  

Finally, you contact support.  "Oh no sorry, we don't have a silent install process.  We just install it manually; our software is really fast it only takes 2 minutes!".

Some choice words under your breath and your perfect application management system is incomplete.

Why is this so hard!  Sure 2 mins is not a lot of time.  But it's not uncommon for IT departments to have a support ratio of users to techs of 100:1 or even as high as 300:1.  So 600 minutes of installing software.  Doesn't sound like a lot but it's not really 600minutes.  It's 2 mins, plus entering configuration of the database manually, hard coding passwords, custom setting files etc.  So let's be generous and say 10mins a PC.  Now we are up to 50hours.  Oh, you think all 300 users are in the same location...yeah they aren't.

!["Aint nobody got time for that"](/images/aintnobodygottimeforthat.jpeg "Aint nobody got time for that")

Why can't developers spend 10mins to create and installer.  There are tons of options to build exactly what we need.  The basic versions are all free.  If you paid for a Visual Studio license, which 80% of you did, you get an install builder included!  This is not a difficult problem to solve is what I'm trying to say.

Server installs are no different.  I've installed million-dollar systems where I'm manually installing files and configuring multiple web sites.  For that amount of money, I expect someone onsite to do it all for me.  Oh wait!  I did have someone onsite, but I was doing it for him as he was not quite sure how to configure a web server on Windows!  

That was about 50hours just for the server.

...and it gets better...

Application Updates
---
Those 50 hours of work you gave to your junior (you bought them a coke right), yeah, a month later there's an update to the software and guess what?  The department NEEDS it.  NOW!  

And the process is as simple as just running the new installer.  It updates the software for you!
Only 49hours more hours left.

What's that? There's monthly updates!?!

!["What!?!"](/images/picard.jpg "What!?!")


A company I worked with recently had software that required all devices to be updated as the server was updated otherwise it wouldn't work.  Not the worst problem, except it was software running on heavy mobile machinary in a plant, and the software ran in tablets in the equipment.

They expected every piece of equipment to stop, come back into the workshops, and be updated otherwise they couldn't record operational data.  The whole place had to stop for a software update.  Downtime there costs a LOT, more than lunch money.

Security Issues
---
Ok you've spent 50hours a month on updates and stopped your entire mine a few times.  You get back to Sysadminin' happily.  You get up to write some guidelines on your IT security policies.  It contains some somewhat standard requirements.

* No Shared Passwords
* No users with Admin access
* All software within vendor support
* All Windows desktops on Windows 10
* All Windows Servers 2016 or newer

That seems all pretty standard and reasonable.  Keep everything secure, minimal security footprints, everything running on a newer version of Windows.  You feel pretty good about yourself for spending some time documenting things and fixing a few small problems.

Then HR stop by.  They have new software for collecting and tracking candidates.  You missed the meeting?  Don't worry it's already purchased. How bad could it be?
You finally get the software.

* "Requires .NET 2.0" - That hasn't been supported since 2011!
* "Admin rights required for each user's desktop" - You ask what it's required for but get a vague "it doesn't work without it" response.

After you install the software, you find it does not correctly assign security permissions to the install folder.  You try manually fixing it to work for non-admin accounts and it works without a problem.  On a roll you even put the fix into your application management system so it's automated!  Now your sysadmining like a pro!

One problem fixed, but .NET 2.0 that can't be fixed.  Not without the source code.  But you persist with the vendor.  Because it's a big fat security hole in your otherwise perfect system.  Microsoft have stopped support, 8 years ago.  I had two kids since then.  Plus, once you install that component it's the whole computer that's compromised by it, not just the HR software.

Inspired by your previous permissions hacking fix, you look through the software, it's components, the third-party libraries it uses, the weird data export function it uses.  Nothing that specifically ties it to version 2.0.  And let's get this straight 4.7.2 is current release and there's been 12 releases between that and 2.0.  This is like driving a car with leaded petrol.

Why does this bother me so much?  Because it reeks of lazy and uninformed programming.  How do you change your .NET framework level in Visual Studio?  There's a simple option in the project properties.  Change it to the latest restart Visual Studio and compile your code.  2.0 might be a bit of an extreme example but believe me I've seen it...recently.  More likely is 3.5 or older versions of 4.  I've never had a developer able to defend the choice, which makes me feel like they honestly don't understand the very system I'm paying them to be an expert at.

Another real-world example:  That super expensive SAP system that's so expensive that it's causing localised hyperinflation in the breakroom.  I've been told by a major support SAP partner in 2018 that it is not supported on Windows 2016 Hyper-V.  Only Windows 2012 R2.  SAP runs on Windows Server 2016, but not on a 2016 hypervisor.

"Really?  Why's that?".  "They don't say why but there must be a good reason.  It's definitely not on the approved hyper-visor list."

Well I'd been running it for at least 18months without an issue.  Or maybe I had an issue and just hadn't discovered it.  I definitely remember watching a Microsoft Ignite Keynote where very senior MS and SAP execs had gone on at length about SAP on Azure and how great it worked there.

{{< youtube rzg-fhGGZCg>}}
Maybe Microsoft Azure is still running 2012 r2...

So the answer to my problems was to build a complete 2012 r2 Hyper-V environment just for my SAP system, separate to the other 70 odd servers that ran perfectly on 2016, which at that point in time included SAP.

The project never continued for other reasons.  But I was secretly going to flat out refuse to do such a dumb thing. Or just run up a standalone hyper-v server of the supported version and then migrate it back to the 2016 cluster as soon as they had finished.

![Not doing that](/images/grumpycat.jpg "Grumpy cat doesn't follow your vendor rules")

One last example:  SCADA/Control systems.  The most conservative of all the software vendors.  

"Windows 2016? Lol! we don't support any version of Windows that new enough to get security patches."

"It also needs the server console logged in to run the software.  We don't do services (can't trust them). If you could have that machine logged into an admin account at all times that would be great." 

"Virtualisation...what's that?"

Turns out, if you try it, it does work, but the vendor won't support it.  *Your millage may vary.

Plain bad software
---
After all of that what are you left with?  Software written by people who don't understand the requirements of corporate IT, that compromises the security of the entire enterprise, needs old operating systems, old frameworks, requires 1000s of hours just to keep it running and for what?  Is the software good?  Short answer No.

How could it be?

If you barely understand what constitutes basic requirements, how can the end-product be great?  It's always full of poor user interfaces, bad license management, terrible data import/export functions, memory leaks, no thought of a backup/restore system and the reporting system is always ALWAYS an excel file.

If software was represented by buildings, most of them would be condemned.  Even Kevin McCloud wouldn't try and rebuild it.

![We will convert this barn our budget is 50c](/images/oldbarn.jpg "We will convert this barn our budget is 50c")


If it was a bridge you'd make up a rumour that the people on the other side of the river where witches and just stay on your side, so you'd never have to put a foot on such a rickety, dangerous contraption.

![She's a Witch!](/images/shesawitch.jpg "Very small rocks")


If it was a sick dog, you'd have pity on it, man up and shoot it in the face.  Sorry old yella.

![Sorry old yella](https://thumbs.gfycat.com/LimpingFaithfulGarpike-small.gif "Sorry old yella")

Ok sorry, that got dark. 


Great software is difficult to write.  I understand that.  But I don't expect it to be great.  I expect it to at least be thoughtful.

Niche software is always guided by industry experts.  It must be.  An IT guy can't write accounting software.  But put an accountant with a developer and mix in some IT corporate experience and then you might get something worthy of that large annual license fee.

It's 2019 and time for software to be better.  All these faults are just basic should be there in version 1.0 problems.  I don't expect to have to install .NET 2.0 or old versions of Java or have admin rights.  I need a silent install package.

Once I get the system in, as an IT guy I want to spend time automating data in and out of your custom system reducing HRs time to find a candidate.  I want to help accountants with their end of month reporting, make it a smooth process, get the data accurate, and get it to managers looking professional.  I get it accountants work hard.  HR guys spend hours finding candidates.  I can help you.  But I spend my life installing updates...I could write symphonies but I'm stuck playing hot cross buns on a recorder.  

You may think I'm being hard.  Far from it.  These, mostly anonymized examples, are from the last 18 months.  But after a career of dealing with it I'm getting fed up.  Software needs to improve everyone's lives.  If it makes our life harder, more complex, then why are we paying you.  How can I go to my executive team and defend it?

Do the hard work in the background, think about end users, make that UI intuitive, make amazing APIs that can integrate data flows in and out of systems, create beautiful reports straight out of the box.

There are some horror stories here and it's been therapeutic to get them off my chest.  But it's not 100% horror.  There are occasional vendors who get it mostly right.  They understand software management in the enterprise.  They are experts in the niche, and when we use your software we are all more productive and it makes our day that bit brighter.  I keep on the look out for those white whales

<img src="/images/callmeishmael.jpg" alt="Not a big Melville fan" title="Not a big Melville fan? He's not an easy read">
