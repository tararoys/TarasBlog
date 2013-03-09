Title: Tara's First Markdown Page
Author: Tara Roys
Date: Tue Feb 25 2013 10:16:51 GMT-0600 (CST)

Node: v0.1.102
lalalala

Why use version control?  

Imagine that you want to get to the top of a fifty-foot cliff.  You could jump up and start climbing.  What happens if you make a mistake?  You fall off the cliff.  This is not a problem when you are three feet off the ground.  This is a big problem when you are thirty feet off the ground.  The problem is, every inch you climb closer to the top, of the cliff, the more dangerous it becomes to you if you make a mistake.  

This has a couple of consequences.  Most people, looking at the cliff, will decide they don't want to die, and choose not to climb it.  Some people will only climb three feet up, because that is how high they feel comfortable going.  Only a very few, very experienced climbers and a few foolhardy people will climb all the way to the top.  The rest are too afraid, and rightly so, that they will break something if they try it.  

And then someone invents a rope.  A climbing rope.  the climbing rope works like this:  a climber climbs a little bit up the cliff, and then puts a bold in the cliff.  They tie a rope to the bolt.  Then they start climbing again.  Now what happens if they fall?  They will fall past the bolt, and the rope will catch them, and they'll swing against the cliff face cursing a few times- but they won't die.  They also won't fall all the way down the cliff.  

What happens then?  People who used to be afraid of falling, people who weren't all that good at climing, will start climbing the cliff, secure in the knowledge that if they do fall, they won't fall that far.  Many, many, many more peopel climb the cliff, and most of them make it to the top.  

Writing a program is like climing the cliff. Every line you write makes your program more complex, and puts you higher and higher on the cliff face.  The more lines you write, the more you're afraid that you will make a mistake that breaks the whole program and leaves you falling, tumbing to the sharp rocks below.  But what if you didn't have to fall that far?  

Version control is your rope that is bolted to the cliffside.  Every time you climb a few feet, add a few lines of working code, you save your work into a new version.  That version is your latest bolt in the cliffside.  Even if you add a bunch of non-working code, even if you let go of the cliff face and fall, you won't fall past your last bolt.  Likewise, you won't lose your latest version.  You can go back to it and start coding in a new direction.  

Not only that, but you can look back and a see a line of all your previous bolts in the cliffside.  If you wanted to, you could climb back down to any of them and start climbing in a new direction.  That is exactly the same advantage version control gives you:  The ability to go back to a lower place in your code, a place you know that worked, and start going from there.  

That's why you use version control.  It's your safety rope.  It's your anchors in the cliff.  And it lets you code fearlessly.  

Why use tests?  

Imagine you are a plumber, and you get called to someone's house.  They are complaining because when they turned on the tap, no water came out.  Obviously, something is wrong.  But what?  

You go back to the water company, and check the pipe that leads to the house.  Water is flowing out through it.  Somewhere, between the water company and the house, the water is disappearing.  

You get out the plans, and find out that there are ten miles of pipe between the water company and house.  You groan.  You are not looking forward to inspecting ten miles of pipe to find a leak, especially since most of the pipes are underground and finding a leak might requre digging them up.  You complain to the water company representative about the days you expect to spend finding a leak in miles of pipe.  

The representative looks at you, and says, "Haven't you heard about the testing system?"  

"Testing sytsem?" You say.  "What testing system?"  

"We have sensors every ten feet of pipe."  The representative says.  "They are pretty simple. We send them a signal, and they tell us if there is water in the pipe or not, and are hooked up to this map.  If a pipe has water, they mark it green.  If a pipe doesn't have water, they mark it red.  Let's run the test."  

They run the test, and the plumber looks at the map.  The pipe from the water company to the house shows mostly green, but under the sidewalk outside the house, it turns red. 

"You'll probably find your leak there."   The company representative said.  The plumber went out, checked, and sure enough, found the sidewalk sagging and a huge muddy puddle from where the broken pipe was leaking water.  

Like our plumber using sensors to find the broken place in the pipe, tests allow us to quickly find the broken places in our software.  Software functions are a lot like sections of pipe.  Data goes in one end and comes out another end.  Many times, as programmers we hook miles of functions together, like a water system hooks miles of pipes togehter.  The trouble is, if we spring a leak, where in our miles of functions is the break?  On the other hand, if we hook sensors to every section of pipe we install, we can find out quickly what sections have water and what sections don't.  Testing functions is the equivalent to sensors on pipes.  We can run a test on a function to see if that section of code is still working.  

Now.  Here's another question.  Suppose you worked for the water company, and your job was of add new pipes to the system.  The water sensors are actually a small section of pipe screwed on to the end of a bigger pipe before it is connected to another pipe.  The pipes are usually buried underground.  Do you think it is easier to install all of the pipes first, bury everything and then install the sensors?  
Or do you think it is easier to install the sensor and the pipe at the same time?  

Since installing sensors would require digging up the pipes, unscrewing them from eachother, putting a sensor in between each pipe, reattatching them, and buring everything again, the answer is clear:  it is far, far better to install the sensors at the same time you install the pipes.  

The same holds true for writing tests for pieces of code.  It is far easier to write a test to test a piece of code at the same time that you are writing that piece of code.  

Finally, let's say our water company wants to dig up the side of the road and and a whole bunc of new pipes.  They know that the new pipes are going to go next to old ones, and want to make sure they don't do something silly like accidently cut a pipe. Fortunately, all of their oldpipes have sensors in them.  So every time they lay a new section of pipe, they check all of the sensors to see if all of the old pipes are still working.  With sensors, they can be sure that their new set of pipes didn't break the old set.  

So, in short:  why use tests? To make sure everything is still working, and to quickly find out when and were things are broken.  

 
The difficulty with learning.  

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

Marking a trail makes it easier for people to learn.  If I didn't have that trail, I could spend weeks, if not months, figuring out a way up the cliff.  Unfortunately, most people are uniformly bad at marking thier own trails, and, if they don't, they'll forget that the people following them can't read their minds, and tellig a newbie "Just dyno it!"  seems like a perfectly reasonable thing to say.  

So how do you go about following a trail?  In real life, on of the easiest trails to make is tracking mud across a clean floor.  All you have to do is dip your boots in mud and start walking.  Folloing the mud trail is equally easy.  A person with muddy feet can only take one step at a time, something nearly all humans can do.  When you are following soemone who is tracking mud, the next step is probably going to be within about five feet of the previous one.  You can quite literally follow it step by step.  

My goal with this project is to leave a series of muddy footprints everywhere I go, so that people can follow exactly what I did where I did it.  I want people to be able to follow me up acliff.  

There are three ways I'm going to leave muddy footprints.  The first way is by using git. Git is a version control system.  (See the rock-climbing-with-a-rope analogy.)  I make a commit (i.e. save a new version) of my code every time I add a few lines I try to add no more than six lines at a time.  Why?  Because git has this wonderful tool called diff, which highlights teh difference between version A and version B of a piece of code. It does this by highlighting them. If I only change no more than six lines at a time, you can quickly see the changes and understand them. It's a lot easier to read six lines of code than, say, sixty.  So each version of my code has no more than six new lines, whcih makes it really easy to see WHAT I did.  

The second way I leave muddy footprints is by testing the code I added.  Let's go back to the plumbing analogy:  A piece of code is like a piece of pipe.  Data flows into the code like water flows into a pipe.  Data comes out of the code like water flows out of a pipe.  Sometimes the data is changed by the code it flows through, and you want to make sure that you get out of the code what you expected.  For example, Lets say you have a pipe that is supposed to filter iron out of water.  Water and iron go in one end, and you expect clean water to come out the other end.  You would add a little iron tester to the pipe to make sure that there is no iron in the water that comes out of the pipe.  A code test tests to make sure that what comes out of your piece of code is what you expected, just like the iron tester makes sure you get clean water out of your pipe.  A test's job, then, is to make sure the piece of code WORKS the way you want it to.  Because it usually does this by trying out the code, a test also serves as an example of how to use the piece of code.  So this particular part of the muddy footprint explains how to use code and checks if it works. 

The third way I leave muddy footprints is in the commit message.  The commit message is so that you can talk about the changes you made.  Since my commits are usually a few lines of code and a test that tests that code, my commit message explains what that change was.  Since I'm using this entire process as a learning tool, I also explain WHY I did what I did and what I learned while doing it.  

So, in short, a single footprint, for me, is a git commit that explains what I did, how to use what I did, how to test what I did, why I did it, and what I learned while doing it.  


There is one final way I intend to leave muddy footprints:  This blog.  Most
novices don't know how to read a git history, which violtates the principle of
not marking your trail with symbols that other people don't understand.  Most
people can read blogs, however.  So I intend to explain each of my footprints
with a blog entry.  This is where I try and make up analogies to explain what I've done, chit-chat about what confused me and teach what I've learned.  

Hopefully, with all of this information, you will no longer feel like I did, stuck at the bottom of a cliff while someone else waves in the distance.   

