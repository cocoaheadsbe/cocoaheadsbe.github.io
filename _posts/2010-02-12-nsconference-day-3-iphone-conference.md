---
title: 'NSConference Day 3 &#8211; iPhone Conference'
author: Stefaan Lesage
excerpt: 'Well, after a brief night it was time for the last day of NSConference which was targetted at iPhone development an developers.  I did notice quite a few new faces on this last day.'
layout: post
permalink: /2010/02/nsconference-day-3-iphone-conference/
thumb:
  - https://cocoaheads.be/wordpress/wp-content/uploads/2010/02/NSConference-180.jpg
categories:
  - Information
tags:
  - Cocoa
  - community
  - Conference
  - Core Animation
  - Drew McCormack
  - GameKit
  - iPhone Development
  - Jeff LaMarche
  - Mac Development
  - Marcus Zarra
  - Mike Lee
  - NSConference2010
  - OpenGL ES
  - ZSync
---
### Meet the User &#8211; Mike Lee

Today started with an opening keynote by [Mike Lee][1]. This time his keynote was awesome. There was plenty of advice in this Keynote. One thing he showed us is that you should target your app at the average user. In fact he said : &#8220;If you are targeting the expert user of your app, you are targeting the wrong user&#8221;. You should actually design your app to do the most common tasks really well, and not a few complicated things which will only be used by 3 or 4 users anyway. He really gave me one piece of advice which I&#8217;ll carry with me and that is &#8220;Know your target user&#8221;. If you know who will be using your application, you will have a pretty good idea on the features they are looking for.

### Hard and Fast OpenGL ES &#8211; Jeff LaMarche

This session concentrated around OpenGL and OpenGL ES. OpenGL ES is apparently a great tool for 2d and 3d drawing, but probably not as easy as Core Animation and Core Graphics. Both OpenGL and OpenGL ES define their own datatypes which are actually the same ones as the default ones but prefixed with GL. For functions there is apparently some specific convention as well. Functions are suffixed with a letter depending on the types of arguments passed to the function.

This was again one of those sessions which made me realize I still have a lot to learn. Still OpenGL and OpenGL ES seems to be quite interesting for Game Development.

### Core Data Synchronization &#8211; Marcus Zarra

Yesterday we had a presentation from [The Big Nerd Ranch][2] in which he mentioned that Data Synchronization would become a very important issue. Wouldn&#8217;t it in face be nice if your twitter client on your desktop would automatically mark tweets as read if you viewed them with the same twitter client on your iPhone ?

Well, that&#8217;s where [ZSync][3] comes to play. ZSync can be used to sync data between your desktop and your mobile phone. Apparently right now syncing from the iPhone to the desktop seems to be working and is 90% finished. For now it has only WiFi syncing though. The goal is to have cloud syncing over 3G or WiFi in the future as well as Mac to Mac syncing and a few other things.

### The Physics of Sumo: Developing Games with Core Animation &#8211; Drew McCormack

[Drew McCormack][4] was back with a session on Core Animation which he used for his Sumo Master game. He did mention though that if you plan to do a game, you should probably take a look at OpenGL instead of Core Animation. But he did show us that you could actually do quite a lot of things with Core Animation too.

To me, this was one of my favorite session. It showed you the power of some of the iPhone API&#8217;s. You can actually achieve some very good looking results with it, and still have code which isn&#8217;t looking all too complex. Drew showed us several stages of the development phase and showed us some pieces of code which he used to solve some animation problems.

### Supporting Online Play and GameKit in your app &#8211; Jeff LaMarche

This last session of NSConference was all about GameKit, which is a framework provided to you that can facilitate easy network play over Bluetoot. It&#8217;s main focus is probably that it&#8217;s designed for networkable games on the iPhone (it can&#8217;t communicate with bluetooth on a desktop machine). Quite interesting for those of us developing games with network play, but apparently you can actually transfer any kind of data with it.

### Closing Words

Well, that concluded the NSConference, and if you ask me if it was worth it&#8217;s money, my answer would be &#8220;Absolutely&#8221;. Not only were the sessions quite interesting, but there was a lot of opportunity to meet up and chat with presenters and fellow developers. I think I probably learned as much from the discussions outside the session room than from those in the sessions. So I would like to take the opportunity to thank [Scotty][5], [Tim][6] and all others who made this conference possible.

The conference actually motivated me to start with my own iPhone application, and although I still have a lot to learn it&#8217;s going quite well. I really hope we will have an European version of NSConference next year to, and if that is the case, I&#8217;ll surely be signing up for it.

 [1]: http://twitter.com/bmf
 [2]: http://www.bignerdranch.com/
 [3]: http://www.zarrastudios.com/ZSync/ZSync.html
 [4]: http://twitter.com/drewmccormack
 [5]: http://twitter.com/macdevnet
 [6]: http://twitter.com/timisted