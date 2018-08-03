+++
date = "2018-02-24T12:00:00-00:00"
title = "Bandwidth and Latency"

+++

Understanding the concepts of bandwidth and latency is important in understanding how networkk and internet connections function and why slow can be ambiguous<!--more-->


Bandwidth
---------

When we talk about bandwidth we are talking about the maximum rend and receive rate for a network or internet connection.  A connection will be spoke about as 2Mb/s or 100Mb/s or even 1Gb/s.  

Think of you connection like a road.  Bandwidth is equivalent to how many lanes you have on the road.  More cars can travel at once  on a 8 lane freeway than they can on a one lane back road.

To reach those speeds applications need to be able send traffic up or down at that speed.  Generally, applications like video streaming do a good job of taking up a lot of bandwidth and can sometimes be a good indicator of speed.  Downloading large files from a website will also help demonstrate speeds.

But remember, on the internet there is not just one road from you to a server or website.  There are likely hundreds of roads of different sizes, so one website or one type of traffic is not always an acurate test.

Having said that, the one test which is usually pretty good for internet is [speedtest](http://speedtest.net)


Latency
-------
 
Latency is the time is takes for information to travel from one location to another.  When we download something from the internet, it has to travel from the server to your computer.  While internet data travels somewhere in the vicinity of the speed of light, that can still be noticable for traffic that comes from halfway around the world.  Now we are talking milliseconds here.  But in the right circumstances it can be a couple of hundred milliseconds which starts to easily translate to half a second or more.  That still might not sound like much, but a skype call with high latency is going to mean a lot of delay.

For Australians this is particularly noticable, as a lot of content exists overseas.  There are ways and means around this issue, and big content providers like Google and Netflix have their own solutions.  But remember that if you have a satelitle connection, it has to travel from earth to geosynchronous orbit 35,786km away and back.  That's a fair way to travel.

Think back to TV presenters and their correspondants "via satelite".  It always takes a few seconds for them to hear the question and start responding.  We can hear them fine ie there is enough bandwidth to send all the data we need.  However, there is high latency, those pesky 35,000km high satelites, and it takes time to for the data to get down the connection.


Putting it together
-------------------

So when someone says their connection is slow, what do they really mean?  Do webpages take a while to download?  Could it be large latency on a website on the other side of the world?  Does it respond quickly to start with but just take a while for all the information to get downloaded?

Now you know the diffence you can understand the overall problem....

***You can increase bandwidth but reducing latency is much harder***