+++
date = "2018-03-22T12:00:00-00:00"
title = "When to host your own server"
+++

After espousing the benefits of the [cloud here](/post/do-i-need-a-server-room), there are some reasons why you'd want to host some of your infrastructure on your own premises.

More and more technologists are shouting **"Cloud Only"** like it's the only option you have.  However, the world is never that black and white, and your IT needs to work on this scale of grey.

A much better philosophy is **"Cloud preferably"**<!--more-->

So my reasons to host your own server

Your location limits your internet
-----------------------------------

While you *can* access the internet from just about any conceivable location on earth these days, not all internet connections cost the same.   If your business is located somewhere remote, you may have to settle for less than stellar internet.  It may be:

* Too slow, either
  * Not enough [bandwidth](/posts/bandwidth-and-latency) ie 2Mb/s vs 100Mb/s.
  * [Latency](/posts/bandwidth-and-latency) is too big to work efficiently
* Unreliability.  Fibre to the premises is the gold standard of connectivity but it's definitely not available in all areas of Australia.  Even then if you have a single fibre strand a failure to *dial before you dig* can put you out of commission pretty quickly.
* Cost is prohibitive.  Maybe you can get the speed you need, but not the amount of data transfer you need for the right cost.

All of these factors are common enough in a lot of regional areas.  While things are improving over time, the sheer size of Australia and lack of population density means that we can never catch up to countries like South Korea.


Do the sums, and weigh up whether that fancy triple redundant, unlimited bandwidth application 200km from civilisation is going to cost more or less than a server in a suitable onsite location.


Your Application is Critical
----------------------------

I've heard enough people tell me there IT is *critical*, but most of the time it isn't.  Sure you'd like to have your email 24x7 but if you didn't have it for an hour late at night will it cost $100k in downtime?  Probably not.  However, there are some systems that are absolutely critical, security systems like access control and CCTV or SCADA control systems.  These can be critical and downtime can cost 6 or 7 figures per hour of outage.


Your Data is Sensitive
----------------------

Some businesses have sensitive data.  I'm not talking emails you don't want competitors to see, I'm talking properly classified secret data with a license to kill type data.  These days cloud providers are becoming certified to host some types of sensitive data, and with privacy protection laws around PII type data (credit cards etc), you might be worth looking into offloading the responsibility to a third-party.  But sometimes you just can't trust people.

When you consider making your choice, think about not only how your data is stored, but how it is transported.  The server maybe triple locked in a secure vault, but if you send your data as a public Facebook status over the internet, you may not have thought it through.


It's your core business 
-----------------------

Maybe your core business is something that only works on your tech that you developed that will one day be hosted in the cloud.  Cool, sounds interesting.  If this is your situation you probably already know if it's going to be on premises or in the cloud.  But is it just something you think is core business but is really something you enjoy "playing with", well technology is fun for some of us, so who am I to argue.  That's something to defend with your financial controller.


But we just bought new gear
---------------------

Sometimes the decision is not purely technical.  Did you just do a large infrastructure refresh?  Have an awesome rack full of new servers?  Great!  Use them.  Think about slowly exploring cloud options without having to go all in at one time.  Change always has a risk to the business.  Don't move just without a great reason.  And remember, one day that shiny new server will be old, slow and not as shiny.  Then you can send it to that big server farm in the sky and move to the cloud.


Think hybrid
-------------

As the saying goes "*Porque no los dos?*" - *"Why not both"*.  You don't need to commit fully one way or the other.  Think about your infrastructure, applications and services to your business.  What makes sense to put in the cloud, what makes sense to keep.  As I said, change always has some associated risk.  For a lot of businesses, hybrid setups may definitely be the best approach.

Remember **"Cloud preferably"** not **first**
