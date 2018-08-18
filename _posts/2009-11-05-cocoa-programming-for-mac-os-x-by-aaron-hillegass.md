---
title: Cocoa Programming for Mac OS X by Aaron Hillegass
author: Stefaan Lesage
excerpt: 'This is the first in a series of book reviews on Mac / iPhone Programming, Objective-C and Cocoa.  This book should get recommended to everyone who is starting with Objective-C and Cocoa. '
layout: post
permalink: /2009/11/cocoa-programming-for-mac-os-x-by-aaron-hillegass/
thumb:
  - https://cocoaheads.be/wordpress/wp-content/uploads/2009/11/CocoaBookCover.jpeg
categories:
  - Book Reviews
  - Reviews
tags:
  - Aaron Hillegass
  - book
  - Cocoa
  - Objective-C
  - programming
  - resource
  - review
---
### Introduction

Coming from the world of Borland Delphi and having about 10 years of experience in that matter, I do already know quite a lot about Object Oriented programming. But I remember my first look at XCode and Objective-C about 3 years back and the whole syntax scared me off very quickly. It was only a few months ago that I decided to buy me some books, delve into them and finally try to learn Mac and iPhone development. I knew I would have to learn the whole language (never really did any C) and of course Cocoa / CocoaTouch.

### The book itself

One of the first books I started to read was [Cocoa Programming for Mac OS X (Third Edition) by Aaron Hillegass][1]. I have seen many good reviews for the book, and apparently [Aaron Hillegass][2] is also one of the teachers at the [Big Nerd Ranch][3]. So finally I bought the book (together with about 6 other books on Mac / iPhone programming) and started to work my way through it.

As I mentioned before, the whole syntax is what scared me off in the first place. Once I got to the third chapter of the book, which gives an introduction to Objective-C, some of the pieces of the puzzle finally came together. I quickly learned about classes and instances (which is actually the same in Delphi), messages (which we call Methods in Delphi), Initializers (Constructors in Delphi) and a lot of other things. I immediately noticed a few differences between Objective-C and Delphi. In Delphi calling a non existing method on a class would cause an error when compiling, in Objective-C it was actually possible to do that (it does cause a warning though), because the system works differently. Apparently you can even send messages to nil.

The whole chapter about Memory Management wasn&#8217;t all that new to me. I did learn about the retain counts, but had actually used something similar to build what I called an Interfaced Development Framework in Delphi, so I quickly knew what the whole thing was about. From my Delphi experience I&#8217;ve always used to Free objects when I no longer needed them and I quickly noticed that it was actually the same thing in Objective-C.

The Chapter on Interface Builder felt somewhat strange to me. Delphi allows you to quickly design a User Interface without you having to write all that much code. But soon I noticed that the IBOutlets were similar to the published variables used by Delphi to allow the UI to reference objects in your code and the IBActions were quite similar to what we call Events in Delphi. Key-Value coding and Key-Value observing were new to me, and so were Categories, Notifications, Delegates and quite a few other things I read in the book. It took me a while to really grasp what Delegates were and how they could be used, but once I compared it to things I knew from Delphi it started to get better.

A Delegate is actually nothing more than a way for an object to expose some behavior publicly, but the implementation of that behavior is left to the associated / delegate class. Comparing that again to what I already know from Delphi, I found out that I had been using that for ages, I just didn&#8217;t know it was called that way.

I successfully worked my way through the book in a few days, trying everything out and advancing in the book. I have to admit that not everything was immediately clear to me, and I&#8217;m quite sure there are still some things I don&#8217;t fully understand. But I am quite sure those things will come once I start to use them.

#### Conclusion

The book was actually a very good start or introduction to Objective-C and Cocoa. It is very well written and understandable even for people like me who don&#8217;t have any previous experience with Objective-C or Cocoa (although experience in other OO programming languages does help). The examples used throughout the book are well done, and explained in detail. The book covers a lot of topics, but don&#8217;t go into all the overwhelming details which would scare you away.

In my opinion, this is a book I would recommend to everyone who is starting with Objective-C and Cocoa. Wether you already know C, but want to learn Objective-C and Cocoa, or you are a windows developer trying to learn how to do it the Mac Way, then this is the book for you !

### Table of Contents

Here is a list of all the chapters covered in the book :

  * Chapter 1. Cocoa: What Is It?
  * Chapter 2. Let’s Get Started
  * Chapter 3. Objective-C
  * Chapter 4. Memory Management
  * Chapter 5. Target/Action
  * Chapter 6. Helper Objects
  * Chapter 7. Key-Value Coding; Key-Value Observing
  * Chapter 8. NSArrayController
  * Chapter 9. NSUndoManager
  * Chapter 10. Archiving
  * Chapter 11. Basic Core Data
  * Chapter 12. Nib Files and NSWindowController
  * Chapter 13. User Defaults
  * Chapter 14. Using Notifications
  * Chapter 15. Using Alert Panels
  * Chapter 16. Localization
  * Chapter 17. Custom Views
  * Chapter 18. Images and Mouse Events
  * Chapter 19. Keyboard Events
  * Chapter 20. Drawing Text with Attributes
  * Chapter 21. Pasteboards and Nil-Targeted Actions
  * Chapter 22. Categories
  * Chapter 23. Drag-and-Drop
  * Chapter 24. NSTimer
  * Chapter 25. Sheets
  * Chapter 26. Creating NSFormatters
  * Chapter 27. Printing
  * Chapter 28. Web Service
  * Chapter 29. View Swapping
  * Chapter 30. Core Data Relationships
  * Chapter 31. Garbage Collection
  * Chapter 32. Core Animation
  * Chapter 33. A Simple Cocoa/OpenGL Application
  * Chapter 34. NSTask
  * Chapter 35. The End

 [1]: http://www.bookdepository.co.uk/book/9780321503619/Cocoa-Programming-for-Mac-OS-X
 [2]: http://www.bignerdranch.com/instructors/hillegass.shtml
 [3]: http://www.bignerdranch.com/