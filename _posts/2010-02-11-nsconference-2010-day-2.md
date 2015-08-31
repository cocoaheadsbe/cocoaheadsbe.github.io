---
title: 'NSConference 2010 &#8211; Day 2'
author: Stefaan Lesage
excerpt: 'Well, the socializing at the bar lasted for a while, so some of us would have loved to stay in bed a little longer.  Most of us did get up in time for the start of the second day though.'
layout: post
permalink: /2010/02/nsconference-2010-day-2/
thumb:
  - http://cocoaheads.be/wordpress/wp-content/uploads/2010/02/NSConference-146-1.jpg
categories:
  - Information
tags:
  - Aaron Hillegass
  - Andy Finnell
  - BNRPersistence
  - Cocoa
  - Code Signing
  - Conference
  - Core Data
  - Dave Dribbin
  - Git
  - Graham Lee
  - Jeff LaMarche
  - NSConference
  - NSConference2010
  - OpenCL
  - SVN
---
### Cocoa Design Patterns that Leverage the Objective-C Runtime &#8211; Jeff LaMarche

[Jeff LaMarche][1] opened the second day, since Matt Gemmell was sick and had to return home. Jeff talked about some main differences in Objective-C and the possibilities of the Runtime. At some point he even mentioned to step away from Copy & Paste, something I&#8217;ve been telling Delphi developers for a few years by now <img src="http://cocoaheads.be/wordpress/wp-includes/images/smilies/simple-smile.png" alt=":-)" class="wp-smiley" style="height: 1em; max-height: 1em;" />

Additionally Jeff gave us some examples of things you can actually do with the runtime like determining the properties, instance methods, class methods and much more while your application is running. If I have to compare it to the good old Delphi, I would think of it of the Delphi RTTI on steroids. He did warn us though that using the Runtime you could get access to stuff Apple doesn&#8217;t want you to see or touch. In case of iPhone programming this could lead to your application being rejected on the AppStore.

### Brushing Up on OpenCL &#8211; Andy Finnell

I have to admit that the session by [Andy Finnell][2] was way too technical and complex for me. The talk was about modeling the process in watercolor spreading using OpenCL. The whole concept of Context, Devices and Queues was a bit too much for me though. I left the session with a strange feeling &#8230; I suddenly knew I still have a lot to learn &#8230; and I had the impression that all painters must be smarter than myself.

### Version Control Shoot Out &#8211; Dave Dribbin

For some reason people in the room were expecting some kind of Mud fight when [Dave Dribin][3] started his sesison on Version Control Systems. There were basically two big camps &#8230; on one side the Subversion users and on the other side the Git users &#8230;

Dave gave us a brief history of VCS and gave us some Pro and Cons on SVN, DVCS and Git. I have always been using Subversion and never really tried Git, but I guess I should give it a shot some day.

### Code Signing &#8211; Graham Lee

Next up was [Graham Lee][4] with a brief session on Code Signing. The goal is to actually sign your application so it is tied to a unique identification. The great example he gave was if Malicious Monster would create a Malicious Library to attack Safari, they can sign as Malicious Monster or not, but can&#8217;t pretend to be anyone else. Apparently that unique ID is also used by other things like Parental Controls. Although this was a short session, I actually found it quite interesting.

### The Many Faces of Data Persistence &#8211; Aaron Hillegass

Many Cocoa developers have heard about [The Big Nerd Ranch][5], and if you didn&#8217;t you have probably read the book Cocoa Programming for Mac OS X by [Aaron Hillegass][6] (see our [review of the book][7]), and if you didn&#8217;t I suggest you go read the book ASAP <img src="http://cocoaheads.be/wordpress/wp-includes/images/smilies/simple-smile.png" alt=":-)" class="wp-smiley" style="height: 1em; max-height: 1em;" />

Aaron gave a talk about Data Persistence, and repeated that everything is moving to the cloud pretty fast. The concept of Files is dead, Long Live the Cache ! In order for our data to live on the cloud, we will need some way to synchronize that data to our local machines. The session wen through many aspects of storing your data and finally ended with Core Data.

Core Data seems to be a ver good solution, but in some cases it can be a little &#8216;slow&#8217;. At first I had no idea what he was talking about. I didn&#8217;t use Core Data yet and never heard it was SLOW ! But then he talked about the BNRPersistence which is available under the MIT license and can be downloaded from the [Git Repository][8]. BNR Seems to be similar to Core Data, but apparently is a lot faster. He showed us some numbers :

  * Fetch 1M Songs BNR 3.6s CoreData 3.1s
  * Insert 1M songs BNR 12s CoreData 56s 5x
  * Fetch 1K playlists BNR 0.4s CoreData 5.6s 10x
  * Insert 1K playlists BNR 1.2s CoreData 12.0s 10x

Depending on the case BNRPersistence appeared to be between 5 and 10 times faster than Core Data. What&#8217;s good is that BNRPersistence works on iPhone as well ! Great news, but I guess I&#8217;ll have to learn Core Data first !

### Cocoa Rumble = Conference Speakers and Guests

I had no idea what to expect here, but the speakers were being teamed up with some people in the audience and got divided into 3 groups. Each group was assigned it&#8217;s Framework (Core Audio, Core Text and Core Image). The goal was to hold a Framework of the Year contets in which each time had a few minutes to create a presentation on why their framework should get chosen as Framework of the Year.

The presentations by all teams were great and fun to watch, but the best presentation was for Core Image and they won the Framework of the Year contest.

### More Socializing, More Food and More Cocoa Talks in the Bar

Well, the day ended like the previous one. Plenty of us ended up in the bar getting a few drinks and talking about our project. This time I decided to get to bed a bit earlier and get some sleep. At least, that&#8217;s what I intended to do !

 [1]: http://twitter.com/JEFF_LAMARCHE
 [2]: http://twitter.com/macgeek02
 [3]: http://twitter.com/DDribin
 [4]: http://twitter.com/iamleeg
 [5]: http://www.bignerdranch.com/
 [6]: http://twitter.com/AaronHillegass
 [7]: http://cocoaheads.be/wordpress/2009/11/cocoa-programming-for-mac-os-x-by-aaron-hillegass/
 [8]: http://github.com/hillegass/BNRPersistence