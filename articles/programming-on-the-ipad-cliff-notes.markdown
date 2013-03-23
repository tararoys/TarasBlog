Title: Javascript and Node.js Programming on the Ipad
Author: Tara Roys
Date: Tue Mar 21 2013 10:16:51 GMT-0600 (CST)
Node: v0.1.102

We all know that you can program for the Ipad...but what about programing ON the Ipad?  Yes, it is possible. I do client-side javascript development and server-side node.js development locally on my Ipad.  Here's how I do it.  

This tutorial assumes you are familiar with a Linux or Mac command line. 

##How to do client-side Javascript Programming on the Ipad.    

Textastic is an easy-to-use code editor with two killer features for HTML, CSS and Javascript development.  The first and most important is the preview button, which lets you view your webpage just like you were viewing it in a web browser. This feature is _the_ killer feature for doing HTML, CSS, and Javascript development on the Ipad, because it means you can actualy run your javascript code to test it out.  With this feature, I've been able client-side web applications entirely in the Ipad.  

The second killer feature is Dropbox support, which lets  you easily move your code to another machine when you are done writing and testing it on the Ipad.  

##How to Add Git Support to Textastic

The one feature Textastic is missing is version control.  For me, the difference between using Textastic as a toy to write small programs and using it to do serious development is version control, so I found a way to hack it into Textastic.  Here's how.    

Jailbreak your Ipad. 
 
Go to Cydia.  Cydia is a webstore automatically downloaded whenever you jailbreak your Ipad.  It lets you get all sorts of applications.  

When in Cydia, download MobileTerminal and Backgrounder.  MobileTerminal is a command line for iOS.  However, MobileTerminal is COMPLETELY useless without Backgrounder.  Backgrounder is an application that lets you run more than one Ipad application at once.  In a normal Ipad, when you hit the home button, an application will shut down, which means that if you hit the Home button while running MobileTerminal, your screen session will be lost and everything you were trying to do will dissappear unless you have Backgrounder running.  Note:  here's something confusing: in Cydia, MobileTerminal is called MobileTerminal. When you download it, it will show up as a black icon with the name Terminal.  They are the same program. Because of this, I will call MobileTerminal Terminal from now on. 
 
If Terminal did not install, you may need to install a package called core-utils.  If you still have trouble, google a tutorial that specifically tells you how to install Terminal on your version of the Ipad.  

Download Git from Cydia.  

You now have all the packages and apps you need to add version control your Textastic files.  Let's set up version control on a project.  

Open Terminal.  You will see a typical command line.  Press and hold the home button until an alert pops up that says "Backgrounding Enabled."  Now when you press the home button, Terminal will continue to run in the background instead of shutting down and destroying your session.  This means that you can switch to Safari whenever you want to look things up.

When you open up Terminal, your command prompt wills say something like. 

     tara's-Ipad: ~ mobile$  

That means you are logged in as the mobile user.  

Now we need to go find where Textastic stashes its documents.  

Type ls.  You will see a bunch of folders.  One of them is named Applications.  This is where IOS stores all of your apps.  

cd into Applications. In your applications folder, type ls.  

You will see a bunch of alphanumeric strings like 

     87AAC602-3DA8-4A6B-B05F-C3495E778ECB

Each of these alphanumeric strings is a folder containing an app.  

We need to find out which one of these folders contains Textastic.  I do this using the find command.  Type 

     find -iname textastic

You will see which folder Textastic is in:  for example, for me the result looked like this:

     ./87AAC602-3DA8-4A6B-B05F-C3495E778ECB/Textastic.app/Textastic


(If find is not installed on your command line, you will need to install the 'find utilities' package from Cydia.)    

cd into the folder.  If you type the first two numbers of the alphanumeric string, you can tab-complete it.  To use Tab on the Ipad, swipe down and left on the screen. (I found this manner of pressing the tab key  annoying, so I went into the terminal settings and changed it.  The terminal settings are the little i in the lower right corner of the screen.  I set tab to equal a double tap on the screen.) 

When you are in the alphanumeric folder, type ls again.  You will see four folders: 

     Documents/ Library/ Textastic.app/ iTunesArtwork iTunesMetadata.plist tmp/

 
We are interested in the Documents folder.  The Documents folder contains a document tree of all of the files in your Textastic App.  
 
Let's pretend that, in Textastic, you have a project folder called MyWebpage where you store your webpage. cd into MyWebpage.  

Type 

    git init

This initalizes a git repository. In english, that means that the folder MyWebpage is now under version control, and you can use all of the normal git commands to save versions of the files and make commits.

You now have a local git repository that you can save your textastic documents.  Now you can switch back and forth between textastic and the command line to commit your edits to your git repository.  You will notice that the git files are visible in textastic.   

##Pushing your local Git repo to github.

It is also possible to push your local repo to github, but there are a couple of gotchas.  First, the github tutorial for how to do it is not going to be much help, because it is focused connecting to github using the https connection protocol.  There are two ways of connecting to github from the command line. One is to use https and one is to use ssh.  Https is newer and easier, but, unfortunately for you, old versions of git don't allow it, and the only version of git availible for the Ipad is an old version of git.  You are going to have to connect using ssh, and that means going through the painful process of setting up a public and a private key.  To do this, you will want to follow [this tutorial](https://help.github.com/articles/generating-ssh-keys)

At one point, it will ask you to copy a key from the 

     'id_rsa.pub' 

file into your github account.  Unfortunately, there is no way that I have encountered to copy text from mobileTerminal to the system pasteboard.  However, all is not lost.  Use the command line to copy 
	
	id_rsa.pub 
	
into a folder in Textastic.  Open the  Textastic app, go to that folder, open the file.  

##Installing a node.js server on the Ipad.  

There is a package on Cydia called Node.  This is node.js.  Install it.  

Once node.js is installed, you can follow [this tutorial](http://www.nodebeginner.org/) to get started.   

Once you've written a hello world node server, and start running it, go to Safari and type 0.0.0.0:8080.  Congrats: you are running a local development server on your Ipad.


