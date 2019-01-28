+++
date = "2019-01-28"
title = "Top 5 Trends of 2019 - Infrastructure as Code"
tags = ["Infrastructure", "Code", "Trend", "2019"]
+++

Recently I saw a post on the sysadmin section of reddit, a tech who was celebrating the decommissioning of the primary mail server at his company.  He was saying goodbye to a server by name and thanking it for its service.  It was a reasonable size project, coordinating a lot of tasks, outages etc.  It paved the way for upgrades to future Exchange versions for him.  He was suitably excited and so he should have been.  A project done well is always a great feeling.

However, through all the congratulations, there were a few voices who reminded us all of the mantra:

> "Servers are cattle, not pets, and definitely not snowflakes"

<!--more-->

It had already been through my head and had to upvoted.

<img src="/images/datacenter-small.jpg" title="Figure 1 - Really Big Unix Server" alt="Figure 1 - Really Big Unix Server" align=right hspace=20 vspace=20>

Way back in the early days of my career, I worked at a major MSP in Sydney.  They bought a datacentre in the bust of the dot com bubble and started consolidating their datacentres into one location.  Departments were all given their orders to move everything to the new location.  Planning started in earnest, however one team hit a snag.  There was a big UNIX server in a datacentre.  A REALLY big one.  Which also meant it was important.  However, fit was extremely reliable.  So reliable, that it did what it was setup to do 24x7 so long, that nobody in this company had ever rebooted the server before.  Nobody knew for certain what the start-up procedure was.  Sure they had a reasonable idea, but they weren't certain.

If you haven't seen BIG UNIX systems boot, you may not get the sense of the problem.  Sure back in the day, we all joked about getting a cup of coffee while your computer booted in the morning.  I've had colleagues you've had smaller sized UNIX systems that took 45mins to boot.  And they were trying to do DR tests.  On different hardware.  That wasn't plugged together in the "right" order. 

Wait 45 mins to boot ... wrong! .... change one cable .... another 45mins.  

My colleague spent a day and all he did was reboot a server 12 times.  Forget getting coffee, you could go for lunch.

So a BIG server, with downtime being critical?  There were some very nervous looking people.

These days servers are different.  Due to virtualisation servers are created for a single service, or application or function.  We scale out, not up.

The paradox has changed.  Servers are cattle.  We don't give them cute names and treat them like one of the family (Pets).  We try to never have a system we don't fully understand and can't possibly touch (Snowflakes).  We are more evolved.  We have ITIL, change management and build documentation.  Sure, we give servers names, but use site codes and numbers, we don't name them after comic book characters.

But this isn't a trend.  It isn't new.  What is new is the next phase of this evolution.

Infrastructure as Code
----------------------

Things are changing, and it's not from ITIL or change management directly, it's your build documentation that's evolving.

Take that build documentation, that has 50 pages of screen shots of application install, some powershell commands and a few registry changes.

Now go back to the vendors documentation, read there notes carefully, and you find you can replace those screen shots with powershell or a script.  Now instead of opening reg edit and making a few tweaks, add that to your script with some simple existing commands. Bingo you've just fully automated a server install.

So how hard is this?  

* Need a domain controller?  It's about 3 lines of powershell.  
* What about MSSQL?  Single command for installation.  
* What about sysadmins of reddit ready to upgrade Exchange?  Well depends on your environment but installation and configuration is all available in powershell ready for you to put together, and has been for some time.

<img src="/images/dlanor-small.jpg" alt="Code" align=right hspace=20 vspace=20>


Now, let's take it further.  Take your script, upload it to Git, BitBucket or whatever your code repository is and you've got a infrastructure as code.

So domain controller in 3 lines of powershell.  That's technically true, but you need to set and IP address, give it a name, set some firewall rules etc.  But here's the beauty of this.  Break down your scripts into small tasks.  Set an IP, set a name, join to domain, setup firewall to your internal standards, make them all scripts.

Now to build a server, it's like baking a cake, take your scripts put them together and you've automated your build.

Why is 2019 the year for infrastructure as code?

Thers's a number of automation tools available now that really make infrastructure automation feasible and easy.  From Ansilbe to Microsoft DSC, to Puppet.  They allow scripts/runbooks, to be put together to automate infrastructure deployments.

Automation is important, and infrastructure as code takes this to the next level.  No more build docs that are hard to follow, or have errors.  Errors are corrected, and a new version of the code is checked in.  You get the benefits of code repositories like, code reviews, unit test and continuous integration. Your infrastructure is in code, which makes it extremely portable.  It's text that you can take anywhere very easily.  To other sites, to a disaster site even.

2019 is the year to spend time taking your automation to the next level.  Take some pages out of the developers handbook and start using their tools in anger, not just supporting them.  As your code repository grows, you will start to reap the benefits of infrastructure as code.

As always if you need help to take things to the next level, make sure you [contact us](contactus)