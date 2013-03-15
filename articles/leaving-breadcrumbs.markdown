Title: Leaving Breadcrumbs
Author: Tara Roys
Date: Tue Feb 15 2013 10:16:51 GMT-0600 (CST)

Node: v0.1.102


I'm following a trail to the foot of a cliff.  The trail is well-marked, although it is a little bit difficult.  I see a person at the foot of the cliff and I want to talk to them, so I hurry. It still takes me a few minutes, but when I get there, the person is gone.  I look up, and I see that she's now at the top of the cliff.  

"How did you get up there?"  I ask.

She looks down back at me, confused.  "Isn't it obvious?"  

"No."  I say.  

"Well,"  She says, "Follow the 5.8 route- the one that starts by that boulder- up to the crack, then chimny up it untill you get to the overhang.  You'll have to dyno the last couple of sections, but it's pretty easy."  

"Huh?"  I say.  

"See, isn't it pretty easy?"  She grins, waves, and leaves. 

The problem here is that she thought she was being perfectly clear:  and to another climber, who knows what 5.8 and chimney and dyno mean, she would have been.  However, to a novice, like me, her words might as well be martian for how well I can understand them. 
 
Learning a new technology is like running up against a cliff, and many times, reading tutorials and blogs is like talking to the person at the top of the cliff.  They alreay know how to get up it, and to them it seems really obvious.  I've seen this in books and blog posts and endless commentary:  experts assume the people reading have a level of background information they simply don't have.  To a novice, it often looks like an expert teleported from the bottom of the cliff to the top of the cliff and forgot to explain all of the steps in between.  

Now, what if the person at the top of the cliff had put yellow paint on her hands and feet?  Everytime she touched the cliff face, she left yellow handprints and footprints.  She would have left a very visible trail- one that could be used to follow her up the cliff.  Instead of a giant step, we get to see all of the little steps she took to get up the cliff.  It would still be difficult, but it would not be impossible, to recreate what she did.  

Marking a trail makes it easier for people to learn.  If I didn't have that trail, I could spend weeks, if not months, figuring out a way up the cliff.  Unfortunately, most people are uniformly bad at marking thier own trails, and, if they don't, they'll forget that the people following them can't read their minds, and telling a newbie "Just dyno it!"  seems like a perfectly reasonable thing to say.  

The biggest problem is that making a trail that a newbie can follow is hard.  I don't do it because it usually takes a lot of extra work.  A paved road is easy to follow, but it takes construction crews months or years to make it.  I'm not going to quit my job to learn how to mix concrete, so the real question is, how can I make it brainlessly easy to leave a trail a newbie can follow?  If it's not easy, I won't do it, and that will strand whatever poor newbie trying to follow me at the bottom of the cliff.  

So how do I make it easy for me to make a trail?  In real life, one of the easiest trails to make is tracking mud across a clean floor.  All you have to do is dip your boots in mud and start walking.  The trail makes itself as you do what you would normally do.  Following the mud trail is equally easy.  A person with muddy feet can only take one step at a time.  When you are following someone who is tracking mud, the next step is probably going to be within about five feet of the previous one.  You can quite literally follow it step by step. 

My goal with this blog is to leave a series of footprints everywhere I go, so that people can follow exactly what I did where I did it.  I even want people to be able to follow me up a cliff.  

There are three ways I'm going to leave footprints for any given project.  The first way is by using Git. Git is a [version control system](../what-is-version-control).  I make a commit (i.e. save a new version) of my code every time I add a few lines I try to add no more than six lines at a time.  Why?  Because git has this wonderful tool called diff, which highlights teh difference between version A and version B of a piece of code. It does this by highlighting them. If I only change no more than six lines at a time, you can quickly see the changes and understand them. It's a lot easier to read six lines of code than, say, sixty.  So each version of my code has no more than six new lines, whih makes it really easy to see WHAT I did.  A commit also requires you to write a message about the changes you made to the code.  The commit message should explain what was done and sometimes why it was done.  

The second way I leave footprints is by [testing the code I added.  Let's go back to the [plumbing analogy](..//what-is-testing) for testing:  A piece of code s like a piece of pipe.  Data flows into the code like water flows into a pipe.  Data comes out of the code like water flows out of a pipe.  Sometimes the data is changed by the code it flows through, and you want to make sure that you get out of the code what you expected.  For example, Lets say you have a pipe that is supposed to filter iron out of water.  Water and iron go in one end, and you expect clean water to come out the other end.  You would add a little iron tester to the pipe to make sure that there is no iron in the water that comes out of the pipe.  A test tests to make sure that what comes out of your piece of code is what you expected, just like the iron tester makes sure you get clean water out of your pipe. 

 A test's job, then, is to make sure the piece of code WORKS the way you want it to.  Because it usually does this by trying out the code, a test also serves as an example of how to use the piece of code.  So this particular part of the muddy footprint explains how to use code and checks if it works. 


There is one third and final way I intend to leave muddy footprints:  This blog.  Most
novices don't know how to read a git history, which violates the principle of
not marking your trail with symbols that other people don't understand.  Most
people can read blogs, however.  So I intend to explain each of my footprints
with a blog entry.  This is where I try and make up analogies to explain what I've done, chit-chat about what confused me and teach what I've learned.  

Hopefully, with all of this information, you will no longer feel like I did, stuck at the bottom of a cliff while someone else waves in the distance.   

