---
title: How to use a custom background image in your grouped UITableView
author: Stefaan Lesage
excerpt: "For those of you who didn't know it ... a few weeks ago I went to the iOS Bootcamp organized by the folks at Big Nerd Ranch Europe. The course was exactly what I needed to get me started on my own app. Some pieces of the Puzzle came together quite nicely during the course, but ... I wanted more."
layout: post
permalink: /2010/11/how-to-use-a-custom-background-image-in-your-grouped-uitableview/
thumb:
  - https://cocoaheads.be/wordpress/wp-content/uploads/2010/12/Logo_Without_Name.png
categories:
  - Information
  - Resources
tags:
  - Cocoa
  - CocoaTouch
  - Custom Background
  - ios
  - iOS Development
  - Objective-C
  - UIColor
  - UITableView
  - UITableViewCell
  - UITableViewController
---
#### Introduction

This is a repost of my [original article][1] which I posted on my own website. But since it is related to iOS development, I thought it might be interesting for the Cocoaheads Belgium folks as well.

<div id="attachment_473" style="width: 210px" class="wp-caption alignright">
  <a href="https://cocoaheads.be/wordpress/wp-content/uploads/2010/11/Default_Grouped_TableView.png"><img src="https://cocoaheads.be/wordpress/wp-content/uploads/2010/11/Default_Grouped_TableView-200x300.png" alt="The default grouped UITableView" title="Default_Grouped_TableView" width="200" height="300" class="size-medium wp-image-473" /></a>
  
  <p class="wp-caption-text">
    The default grouped UITableView
  </p>
</div>

#### The default Grouped UITableView looks nice but &#8230;

Well, you can use the UITableView in it&#8217;s Plain mode, but also in a Grouped mode. The Grouped mode uses some kind of pattern as the background for the UITableView. It looks quite nice and is made up of alternating light and darker blue-grayish lines.

#### I wanted someting a little more &#8216;Special&#8217; &#8230;

Although the default look isn&#8217;t all that bad &#8230; I wanted to have something &#8216;special&#8217; for my application. So I was wondering if there was some way to change the color used in that pattern. Since I didn&#8217;t know the answer myself, I sent out a tweet. I was hoping someone would pick it up and maybe let me know where I could find some more information on this topic.

#### The feedback I got

I did receive some feedback to my tweet: &#8216;[Is there an easy way to create your own UIColor which looks like the &#8216;Group Table View Color&#8217; but with another color scheme ? #iphonedev][2]. One of the answers was from [Amar Kulo][3] who suggested to supply me with some Photoshop files I could modify.

A few moments later, Amar Kulo even provided me with a complete answer and [wrote a blog post about it][4] to help me out. It is actually pretty easy, so I thought i would share it with the world as well.

#### The Trick

It is actually quite easy to get your own custom background. You simply have to use a custom background image. Amar provides a few samples in his blogpost. The only thing you need to do is open up your favorite Image Editor (in my case Pixelmator), change the colors to you liking and create the necessary versions for your application. 

#### The Code

Once you added the resources to your project, you can simply start using them as the background for your Grouped UITableView. In my case, it was simple a matter of setting the background color in the ViewDidLoad of my UITableViewController :

`
<pre>- (void)viewDidLoad 
{
    [super viewDidLoad];

    // Uncomment the following line to display an Edit button in the navigation 
    // bar for this view controller.
    // self.navigationItem.rightBarButtonItem = self.editButtonItem;
	UIImage *img = [UIImage imageNamed:@"BG_Pink"];
	[[self tableView] setBackgroundColor:[UIColor colorWithPatternImage:img]];
}
</pre>
<p>`

#### Feedback

<div id="attachment_474" style="width: 231px" class="wp-caption alignright">
  <a href="https://cocoaheads.be/wordpress/wp-content/uploads/2010/11/Result.png"><img src="https://cocoaheads.be/wordpress/wp-content/uploads/2010/11/Result-221x300.png" alt="I ended up with this Bakcground and Color Scheme" title="Result" width="221" height="300" class="size-medium wp-image-474" /></a>
  
  <p class="wp-caption-text">
    I ended up with this Bakcground and Color Scheme
  </p>
</div>

Well &#8230; This might not be the best way to do it, so if you have any suggestions, feel free to let me know.

Personally, I had to experiment a bit with quite a few different colors before I got something which did looked OK to me, so feel free to experiment as well, and let me know what you come up with

Next time I&#8217;ll be delving a little deeper into some more things I did with my UITableView and UITableViewCell &#8230; but for now &#8230; feel free to post a comment and have a look at the result :

 [1]: http://bit.ly/hAUp8n
 [2]: https://twitter.com/StefaanLesage/status/2335617765613568 "Is there an easy way to create your own UIColor which looks like the 'Group Table View Color' but with another color scheme ? #iphonedev"
 [3]: http://blog.amarkulo.com "Amar Kulo"
 [4]: http://blog.amarkulo.com/custom-colored-grouped-uitableview-background-image-in-photoshop "wrote a blog post about it"