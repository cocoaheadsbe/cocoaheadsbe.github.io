---
title: Making you code easier to maintain using Objective-C Categories
author: Stefaan Lesage
excerpt: "Well, as you all might know by now, I'm trying to take my first steps in iOS development. And if you read my previous post, you have already noticed that I was playing with some color schemes. After a while though I ended up settting my colors in all different kinds of places. When I wanted to change one color, I noticed I had to modify my code in 10 or more places. Sure, there must be an easier way to write more maintainalbe code, and Categories seem to be helping quite a bit."
layout: post
permalink: /2010/12/making-you-code-easier-to-maintain-using-objective-c-categories/
thumb:
  - http://cocoaheads.be/wordpress/wp-content/uploads/2010/12/Logo_Without_Name.png
categories:
  - Information
  - Resources
tags:
  - Categories
  - Cocoa
  - CocoaTouch
  - ios
  - iOS Development
  - Objective-C
  - UIColor
  - UITableView
  - UITableViewCell
  - UITableViewController
---
### Introduction

This is a repost of my [original article][1] which I posted on my own website. But since it is related to iOS development, I thought it might be interesting for the Cocoaheads Belgium folks as well.

### Colors Everywhere

Well, after my previous post I continued doing some more work on my UI and trying to create my own Style for UITableViews and UITableViewCells. I ended up using the same colors over and over again in all different places in my application. In the end I had code in my UITTableViewController which set the Color for the Background and the navigation bar :

    - (void)viewDidLoad 
    {
        [super viewDidLoad];
    
        // Uncomment the following line to display an Edit button in the navigation bar
        // for this view controller.
        // self.navigationItem.rightBarButtonItem = self.editButtonItem;
        [[self navigationController] navigationBar].tintColor = [UIColor brownColor];
        UIImage *img = [UIImage imageNamed:@"BG_Pink"];
        [[self tableView] setBackgroundColor:[UIColor colorWithPatternImage:img]];
    }
    

This was all working out quite nicely &#8230;

### Using the same color scheme in other Views

<div id="attachment_496" style="width: 210px" class="wp-caption alignright">
  <a href="http://cocoaheads.be/wordpress/wp-content/uploads/2010/12/Input_ColorScheme.png"><img src="http://cocoaheads.be/wordpress/wp-content/uploads/2010/12/Input_ColorScheme-200x300.png" alt="Data Entry View with ColorScheme" title="Data Entry View with ColorScheme" width="200" height="300" class="size-medium wp-image-496" /></a>
  
  <p class="wp-caption-text">
    Data Entry View with ColorScheme
  </p>
</div>

Of course, my application consits of a few different UITableViews and I even added a data entry View and a detail view. As you can see, the data entry view is using the same background color for the UITableView and the UITableViewCells are using the same color as my other UITableView as well.

At some point, I wanted to change the color scheme I was using (it was more pinkish at the start), and use something more Orange or brown like. Sadly this required me to change the color in every spot where I was using it. When I tested it on my phone, it looked horrible, since I forgot to change a few colors.

Since I&#8217;m still developing some basic ideas for the app, and the color scheme might change a few times during the Development cycle, I started thinking. There surely must be an easier way to handle this, which wouldn&#8217;t require me to change the colors in 10 different places.

Of course, I could subclass UIColor and add my own colors to it, but I wanted to try a different approach

### The Categories Approach

During the iOS bootcamp I took at Big Nerd Ranch Europe a while back, we touched on the subject of Categories. Categories allow you to extend a class without the need to Subclass it. Using Categories I could quickly add a few methods to UIColor whithout the need to create a new Subclass.

### Creating a Category in UIColor

Creating a new category is actually quite easy. In my case, I wanted a category on UIColor so I could extend it. I created a new Header and Implementation file and called it *UIColor+MyApp.h* and *UIColor+MyApp.c*

#### The Header File

In the Header file *UIColor+MyApp.h* I added the following code :

    
    //
    //  UIColor+MyApp.h
    //
    //  Created by Stefaan Lesage on 11/11/10.
    //  Copyright 2010 Devia. All rights reserved.
    //
    
    #import <Foundation/Foundation.h>
    
    @interface UIColor (MyApp) 
    
    + (UIColor *)myTableViewBackgroundColor;
    + (UIColor *)myTableCellBackgroundColor;
    
    @end
    

This simply declares a category MyApp on UIColor, and defines 2 new methods on it. *myTableViewBackgroundColor* which will return the Default color which should be used as the background for my UITableViews, and *myTableCellBackgroundColor* which defines the default color which should be used as the background for my UITableViewCells (and in some other places in my app).

#### The Implementation

In the Implementation file *UIColor+MyApp.m* I added the following code :

    
    //
    //  UIColor+MyApp.m
    //  Phocation
    //
    //  Created by Stefaan Lesage on 11/11/10.
    //  Copyright 2010 Devia. All rights reserved.
    //
    
    #import "UIColor+MyApp.h"
    
    @implementation UIColor (MyApp)
    
    + (UIColor *)myTableViewBackgroundColor
    {
        UIImage *img = [UIImage imageNamed:@"BG_Pink"];
        return [UIColor colorWithPatternImage:img];	
    }
    
    + (UIColor *)myTableCellBackgroundColor
    {
        return [UIColor colorWithRed:255/255.0 green:240/255.0 blue:255/255.0 alpha:100];
    }
    
    @end
    

Well the implementation is pretty straightforward. For the *myTableViewBackgroundColor*, I simply return a UIColor based on the pattern in my previous post. The *myTableCellBackgroundColor* then returns the light pink / purple color which gets used as the background for my UITableViewCells.

### Using the Category

Using the Category is now pretty Straight Forward. In my Detail View for example, I have a reference to a UITextField called nameTextField and to the tableView beneath it. So in my viewDidLoad I have the following code :

    
    - (void)viewDidLoad 
    {
        [super viewDidLoad];
    
        /* Load our HeaderView if Necessary */
        [[self view] setBackgroundColor:[UIColor myTableViewBackgroundColor]];
        [[self tableView] setBackgroundColor:[UIColor myTableViewBackgroundColor]];
        [nameTextField setBackgroundColor:[UIColor myTableCellBackgroundColor]];
    }
    

Quite simple, isn&#8217;t it ?

### But what are the advantages ?

For me, it makes my code a little more readable (that is of course a more personal opinion), but what&#8217;s even better is that my code is a lot easier to maintain. If for some reason I want to change my color scheme to use another pattern or another color for the UITableViewCells, I only need to update the code in one sport. Simply modify the Implementation found in UIColor+MyApp.c, build and it&#8217;s done !

Once I found the advantages of this approach, I even added more methods to my UIColor+MyApp category. It now also contains methods which return the color I will be using for the UINavigationBar tine, colors I will be using for different texts in my application, &#8230;

### Feedback

As with my previous post, there might be better ways to achieve the same thing. If you have a more appropriate approach or solution, feel free to let me know &#8230; I&#8217;m eager to learn <img src="http://cocoaheads.be/wordpress/wp-includes/images/smilies/simple-smile.png" alt=":-)" class="wp-smiley" style="height: 1em; max-height: 1em;" />

 [1]: http://bit.ly/dFX9EK