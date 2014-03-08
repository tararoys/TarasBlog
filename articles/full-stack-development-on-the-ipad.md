Title: How do I learn web programming when all I have is an Ipad? 
Author: Tara Roys
Date: Wed Mar 07 2014 10:16:51 GMT-0600 (CST)
Node: v0.1.102

How do I learn web programming when all I have is an Ipad? 

Once upon a time, I dreamed of being a web developer.  All I had was an ipad.  This blog you are reading?  It was developed entirely on my ipad.

For you newbies, rest assured, if all you have is an ipad, it is possible to become 'a full stack developer.'

For you developers, I'm going to brag shamelessly: I installed a full stack, and I was able to develop locally, entirely offline, on my ipad. 

Here's the stack:

  - Editor: TexTastic
  - Version control: Git
  - Terminal: the jailbroken ipad terminal
  - Depolyment server: Digital Ocean
  - Fully automatic deployment:  I push to git, and using git hooks, my sever pulls the latest version of my app to my digital ocean server. 
  - App: My personal blog, running on a Wheat, a node.js blogging engine developed by Tim Caswell

I haven't heard of anyone else who has done so.  Doing so is horribly painful and the only reason you would do it in the first place is if you're a newbie who doesn't know any better.  Oh? Did I mention? I tacked all of this together without knowing what 'a full stack' was.  Behold my hacking skills! 

#Becoming a Front End Developer

Doing front-end development on an ipad is actually less unpleasant than you would expect, and it's entirely due to one man, Alexander Blach, and one program, Textastic.

Textastic allows you to do write and preview webpages.  Basically, it lets you write html, Javascript, and Css.  Buy it from the app store for $8.99, and congratulations!  You have all of the tools you need to be a front-end developer.  It's as easy as that. 

Learning how to code is an entirely different story.  However, at least you have all of the tools nicely made and prepackaged for you. 

#Becoming a Back End Developer

I would describe becoming a back end developer on an ipad as about as painful as getting run over by a truck several times.  You'll see why in a bit.

For a full web-development stack, you're restricted to using javascript and node.js. 

So to get javascript and node.js working, here's what you do.

Step 1: Jailbreak your iDevice.

Step 2: open Cydia. Install the following packages:

  - MobileTerminal- this installs the command line terminal you will run Node.js from.

  - Node- this installs Node.js

  -  Vi iMproved- this is your code editor.

  - Backgrounder- this allows multiple apps to run in the background of your device. This is especially necessary when working with the Terminal, because you don't want to shut down your session every time you go to another app.

  - Git- You can also install git if you want to version-control your stuff.

Voila! you can now do server side programming on your i-device. 

Ok, now you have all of the tools.  How do you actually use them?

Here's where we get to the horribly painful part:

Every time Apple deploys an upgrade to their systems, they plug the security holes that make jailbreaking possible.  This means that for extended periods of time, sometimes lasting weeks, sometimes lasting months, and right now, possibly up to a year, jailbreaking simply isn't possible.

Because Apple and the government consider jailbreaking a bad thing, jailbreaking is utterly unsupported and by some legal interpretations is illegal.  Because the people who download jailbreaks and the people who make jailbreaks must face the distinct possibility of being jailed, the ecosystem supporting jailbreaks is getting more and more underground. 

In short, once you manage to jailbreak your system and get everything downloaded, it is very likely that you will NOT be able to wipe your machine and start over if you break something. This means that development on your ipad breaks a cardinal rule of being able to recover from serious system errors: there is no way to 'back up' your current setup, if you break your machine and have to wipe it, the latest operating system is downloaded and installed by default, and it is very likely that you will not be able to jailbreak again.

Sorry, apple. Android is lookig more and more attractive every day.

Still, let's see if it is possible: 


I'm halfway through the programming tutorial Node Beginner Book and have had no problems running everything on my ipad. See http://www.nodebeginner.org/

For client-side programming, you can program in javascript using the excellent code editor Textastic, which allows you to preview your javascript code and save it to dropbox. There's an iphone version as well, although it does not work on older devices. If you want to program in javascript on your iphone, use the very very simple-minded program JSAnywhere. It lets you program one html page, one css page, and one javascript page in a single program at a time, which is just fine for making small javascript toys.

For other programming languages, ruby is available through cydia as a command line interpreter, although I haven't been able to get RAILS working. Python is also available, and long ago and far away I did manage to install gcc and run c code on my iphone, although I had the help of an expert and now I don't remember how to do it.

So. In short, it is possible to do a few different programming tasks on the iphone. A word of warning- programming with the ipad on the terminal is very very slow. As far as I know, there is no way to paste from the system buffer into the terminal, so you have to type everything out by hand. On the other hand, typing everything in by hand makes you learn it a lot better, so I've found that little problem rather useful. The ipad also makes it impossible to have more than one window open at once, so you really concentrate on your coding.



