Title: What Is Unit Testing and Test-Driven-Design?
Author: Tara Roys
Date: Sat March 9 2013 10:16:51 GMT-0600 (CST)

Node: v0.1.102

Everyone seems to agree that Unit Testing and Test-Driven-Design are good things, but nobody seems interested in explaining what they are in terms that I, a testing newbie, can understand.  After fighting my way through a few tutorials, I came up with the following analogy: A program is like a bunch of leaky pipes, a programmer is like a plumber, and tests are like sensors in the pipes that help you find the leak.

##The Story of Plumber and the Leaky Pipes

Imagine you are a plumber, and you get called to Mrs. Smith's house.  Mrs. Smith is complaining because when she turned on the tap, no water came out.  Obviously, something is wrong.  But what?  

You go back to the water company, and check the pipe that leads to the house.  Water is flowing out through it.  Somewhere, between the water company and the house, the water is disappearing.  You think, there must be a leak somewhere.  But where?   

You get out the plans, and find out that there are ten miles of pipe between the water company and house.  You groan.  You are not looking forward to inspecting ten miles of pipe to find a leak, especially since most of the pipes are underground and finding a leak might requre digging them up.  You complain to the water company representative about the days you expect to spend finding a leak in miles of pipe.  

The representative looks at you, and says, "Haven't you heard about the testing system?"  

"Testing sytsem?" You say.  "What testing system?"  

"We have sensors every ten feet of pipe."  The representative says.  "They are pretty simple. We send them a signal, and they tell us if there is water in the pipe or not.  All the sensors are hooked up to this map of all the pipes.  If a pipe has water, they mark it green.  If a pipe doesn't have water, they mark it red.  Let's run the system."  

They run the test, and the plumber looks at the map.  The pipe from the water company to the house shows mostly green, but under the sidewalk outside the house, it turns red. 

"You'll probably find your leak there."   The company representative said.  The plumber went out, checked, and sure enough, found the sidewalk sagging and a huge muddy puddle from where the broken pipe was leaking water.  The plumber is estatic.  Instead of spending days finding the leak, it took him five minutes.  

#Tests are Like Sensors

Like our plumber using sensors to find the broken place in the pipe, tests allow us to quickly find the broken places in our software.  Software functions are a lot like sections of pipe.  Data goes in one end and comes out another end like water goes in and comes out of a pipe. Programmers hook hundreds of functions together the same way that a plumber hooks together miles of pipe.  So what happens if you put data in a program, but nothing comes out of it?  Most programmers feel exactly the same way as our plumber dreading the idea of inspecting miles of pipe:  They know they have to search all of the functions between the data input and the data output, looking for the broken connection, and they know it is going to take FOREVER.  But what happens 

 One simple way to test a function is to check if there is data coming out of it, like a sensor can check if there is water coming out of a pipe.  Many times, as programmers we hook hundrends of functions together  like a water system hooks together miles of pipes.  It also has the same problems as our plumber:  if we spring a data leak, where in our miles of functions is the break?   If we hook sensors to every function, sensors that test if the data is flowing, we can find out where the break is as easily as the water company rep found the leaky pipe. 
  

Now.  Here's another question.  Suppose you worked for the water company, and your job was of add new pipes to the system.  The water sensors are actually a small section of pipe screwed on to the end of a bigger pipe before it is connected to another pipe.  The pipes are usually buried underground.  Do you think it is easier to install all of the pipes first, bury everything and then install the sensors?  
Or do you think it is easier to install the sensor and the pipe at the same time?  

Since installing sensors would require digging up the pipes, unscrewing them from eachother, putting a sensor in between each pipe, reattatching them, and burying everything again, the answer is clear:  it is far, far better to install the sensors at the same time you install the pipes.  

The same holds true for writing tests for pieces of code.  It is far easier to write a test to test a piece of code at the same time that you are writing that piece of code.  

Finally, let's say our water company wants to dig up the side of the road and and a whole bunch of new pipes.  They know that the new pipes are going to go next to old ones, and want to make sure they don't do something silly like accidently cut a pipe. Fortunately, all of their old pipes have sensors in them.  So every time they lay a new section of pipe, they check all of the sensors to see if all of the old pipes are still working.  With sensors, they can be sure that their new set of pipes didn't break the old set.  

So, in short:  what is testing?  Testing is a method make sure everything is still working, and to quickly find out when and were things are broken. 

I'll also add another observation:  testing keeps programmers sane.  How?  Testing helps prevent situations like our poor plumber, facing the prospect of days of searching miles of pipe for a leak.  Testing not only saves time, but countless hours of frustration, agony, and, occasionally, dispair.  

 


