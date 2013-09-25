Title: Intro To Fractals: Making An Angel's Wing in Chaotica
Author: Tara Roys
Date: Wed Sept 12 2013 10:16:51 GMT-0600 (CST)
Node: v0.1.102

Making Angel Wings: An Introduction to Apophysis
===============================================

Introduction
============

![](wing-Chaotica/wingtutorialcolored3.jpg)

This tutorial assumes you have zero knowledge of fractals or of
Chaotica.

You can use Chaotica with any operating system.  The latest version 
of Chaotica can be downloaded from [the Chaotica Website.](http://chaoticafractals.com/)

This chapter will teach you how to make the fractal wing shown above.  By the end of 
it, you will know how to use the most important parts of the Chaotica user interface, 
and you will have a lovely picture to show off to your friends.  

This tutorial will tell you how to do make a wing.  It will NOT explain the principles behind fractals or Chaotica.  Think of it like a cook-book recipe: a recipe tells you how to make a loaf of bread, but it does not tell you about the science behind bread-making.  If you want to know the principles of specific fractals, see ![](http://www.acm.uiuc.edu/~troys2/ApophysisUserManual/).  This tutorial is adapted from tutorial 1 of that book.  You can use the same principles explained in that book to use chaotica.  


The Main Screen
===============

This tutorial is a general introduction to Chaotica. It introduces all
of the important aspects of the program by teaching how to make an
angels wing. So, without further ado, let me present "How to Make An
Angel's Wing" by yours truly, [Tara
Roys.](http://tararoys.deviantart.com)

![](wing-Chaotica/parameterbrowser.png)
First, open up Chaotica. You will see nine pretty fractals shown in a window 
called the Parameter Browser, like the ones above.  The ones you see will not be exactly like the ones shown here.  Don't worry about 
it.  Double-click on one that you like, and close the parameter browser.    

![](wing-Chaotica/chaoticamain.png)

You will now see the main screen, as shown above.  There are lots of options on the main screen.
At the moment, we only care about one option: AA Level.  

![](wing-Chaotica/SSFactor_1.png)

On the left-hand side of the screen, you will see an option called SS Factor in the Resolutions and Channels section. (It is highlighted in orange in the image above.) Set it to 1. This makes the program draw the fractal faster. 

![](wing-Chaotica/mainmenu.png)

Turn your attention to the main menu, shown above.    

![](wing-Chaotica/openWorldEditor.png)

In the main menu, click on Window and then World editor to open the world editor. 



Moving Your Fractal: The World Editor
=========================================

![](wing-Chaotica/WorldEditor.png)

This is the World Editor.  This is where you can change the shape of your fractal. You will learn to love the World Editor, because this is where you will spend most of your time.



Moving around in the World Editor
-------------------------------------

![](wing-Chaotica/blackgrid.png)

When you open the world editor, the first thing you'll see is
probably a large black screen with a bunch of angles and a grid on it.

The first thing you'll want to learn is how to move around in this
window.

Right-click and hold on the black grid.  Still holding the right mouse button down, move your mouse around. 
You'll drag the grid around. This lets you reposition your editor window so that you
can concentrate on whatever part you want.

To zoom in and out of your editor window, hold down ALT and the right mouse button, then drag the mouse around. Dragging the mouse up will zoom in, whereas dragging the mouse down will zoom out.  

Making a New Flame
------------------------

You'll notice that the picture above has a lot of colored angles pointing every which way. When click on one of the arrow and drag it around, you'll notice that you change how the fractal looks.

Right now, having so many angles pointing every which way is confusing.  We want to delete all but one set of angles and start over.  You can do it by hand, but I'm assuming you want to get on with actually making the wing and skip a lot of the boring setup.  So do the following.  Copy all of the code in the black box below.  

	<flam3_IFS name="New Blank Flame">
		<camera>
			<vec4 name="pos">0 0 0 1</vec4>
			<vec2 name="rotate">0 0</vec2>
			<real name="scale">354.44323</real>
		</camera>
		<imaging name="Imaging">
			<int name="image_width">739</int>
			<int name="image_height">680</int>
			<int name="image_supersample">2</int>
			<string name="antialiasing_mode">strong</string>
			<real name="brightness">4</real>
			<vec4 name="background_colour">0.1 0.1 0.1 1</vec4>
			<real name="flam3_gamma">3.6</real>
			<real name="flam3_vibrancy">1</real>
			<bool name="flam3_use_highlight_power">false</bool>
			<real name="flam3_highlight_power">0.003</real>
			<real name="flam3_gamma_linear_threshold">0</real>
		</imaging>
		<colouring>
			<curve name="hue">
				<table name="knots">
					<values>0 0.14285715 0.2857143 0.42857143 0.5714286 0.71428573 0.85714287 1</values>
				</table>
				<table name="values">
					<values>0.5918913 0.7190439 0.8071572 0.81106025 0.65890545 0.594399 0.8666091 0.037801243</values>
				</table>
			</curve>
			<curve name="saturation">
				<table name="knots">
					<values>0 0.14285715 0.2857143 0.42857143 0.5714286 0.71428573 0.85714287 1</values>
				</table>
				<table name="values">
					<values>0.4825611 0.48530185 0.68892235 0.8892659 0.8779499 0.77066433 0.361463 0.88338655</values>
				</table>
			</curve>
			<curve name="value">
				<table name="knots">
					<values>0 0.14285715 0.2857143 0.42857143 0.5714286 0.71428573 0.85714287 1</values>
				</table>
				<table name="values">
					<values>0.64102125 0.24434546 1.1120775 0.45385367 0.52433705 0.6024935 0.5572967 0.8918465</values>
				</table>
			</curve>
		</colouring>
		<node name="iterators">
			<iterator name="Iterator 0">
				<flam3_transform name="flam3 transform">
					<affine2 name="Pre affine">
						<real name="x_axis_angle">0</real>
						<real name="x_axis_length">1</real>
						<real name="y_axis_angle">90</real>
						<real name="y_axis_length">1</real>
						<vec2 name="offset">0 0</vec2>
					</affine2>
					<node name="transforms">
						<transform name="xform">
							<string name="type_name">linear</string>
							<params>
								<real name="linear">1</real>
							</params>
						</transform>
					</node>
				</flam3_transform>
				<flam3_shader name="Shader">
					<real name="palette_index">0</real>
					<real name="blend_speed">0.5</real>
					<real name="opacity">1</real>
				</flam3_shader>
				<weights_selector name="weights">
					<real name="base_weight">1</real>
					<node name="per_iterator_weights">
						<real name="iter 0 weight">1</real>
					</node>
				</weights_selector>
			</iterator>
		</node>
	</flam3_IFS>


Go to Chaotica.  In the edit menu, hit 'Paste XML from Clipboard.'

![](wing-Chaotica/PasteFlame.png)

You will see a square slowly take shape in the main window.  

![](wing-Chaotica/NewBlankFlame.png)

Now we can start building our wing!



### Moving a Pre-Affine Transform With The Mouse

If you go to the world editor, you will see the following:

![](wing-Chaotica/BlankFlameIterator.png)

Click on the red thing that looks like a pair of arrows coming out from a point.  That thing is called a Pre-Affine Transform. 

 Note: A lot of people like to shorten it an call it a transform because 'Pre-Affine Transform' sounds long and scary.  However, for the rest of the tutorial I'm going to call it by it's full name: Pre-Affine Transform. Why? Because there are six different things in Chaotica labeled 'Transform,' and I don't want you to get confused about which one I'm talking about. Don't worry about the scary-sounding name for now.  

Click on it.  You should see two things.  First, the Pre-Affine Transform is highlighted on the grid, like so: 

![](wing-Chaotica/Pre-AffineTransformHilighted.png)

Second, you will see the name pre-affine higlighted in orange in the iterators panel in the upper-right-hand corner of the world editor, like so:  

![](wing-Chaotica/Pre-AffineHilighted.png)


Let's get this thing moving!

If you've ever worked with Photoshop or a similar image editor, you know that you can move an image in several different ways.  Take a look at the picture below.  The green shape is the original shape, and the yellow shape is moved in some way.  Each particular type of movement is has it's very own fancy technical term that sounds all scary and strange, but really, they're just names for the very ordinary sorts of movements you'd want to do to a picture.  

![](wing-Chaotica/AffineTransform.png)

Taken together, these five movements are called Affine Tranformations, which is where the 'Affine' part of 'Pre-Affine Transform' comes from.  Let's learn how to do these five movements to our pre-affine transform.  

### Translation

Look at the Pre-Affine Transform.  You'll notice that they are made of two arrows. In math terms, an arrow is called an 'axis.'  I am going to use the term 'axis' instead of 'arrows' for the rest of the tutorial. 

Look at where the two axises meet.  There is a small circle that looks like this: 

![](wing-Chaotica/origin.png)

This circle is called the origin.  Click and drag it.  

Clicking and dragging on the origin allows you to translate the Pre-Affine Transform.  

Now is a good time to point out the white axises.  The white axises are the Reference Axises that tell you how far away from the center of the picture you have moved your Pre-Affine Transform.

![](wing-Chaotica/Translation.png)

In this picture, I have moved the Pre-Affine Transform down and to the left of the Reference Axises.  

### Rotation

Look at the Pre-Affine Transform. You see how each axis is made of a circle, a long line, and an arrowhead?  Click and hold on the long line, as shown below, and drag your mouse.  


![](wing-Chaotica/Rotation.png)

This will rotate the Pre-Affine Transform.  

### Scale

You see the box that shows up around the Pre-Affine Transform when you click on it?  Move the mouse to one of the corners of that box.  While clicking and holding your mouse, drag the corner around.  Your Pre-Affine Transform will get bigger or smaller.  


![](wing-Chaotica/Scale.png)

### Skew	

Now look at the arrowhead at the top of the Y axis (The Y axis is the axis with a y by it.)  Click and hold and drag it around.  This skews the Pre-Affine Transform, as shown below.  

![](wing-Chaotica/Skew.png)


### Reflection


There isn't actually a separate reflection widgit in Chaotica.  However, you can drag the arrowhead of an axis so that it is on the opposite side from where it started.  

![](wing-Chaotica/Reflection.png)


We now know how to move the transforms around.  Now that we know how to move one transform, let's give ourselves a few more transforms to play with.

### Adding More Iterators

In the top left corner of the World Editor is a button called New Iterator. It looks like this:  ![](wing-Chaotica/NewIteratorButton.png)

Press it twice to add two new Iterators to your World Editor.  

Note: Iterators are the workhorses that generate the fractal.  What is the difference between a Pre-Affiine Transform and an Iterator?  The Pre-Affine Transform that we're talking about is a part of the Iterator, in the same sense that a spark plug is part of a car.  

Now that we have three iterators, let's start moving them around so that they form a wing shape.

### Creating the Wing Shape

In order to make a fractal that looks like a wing, you need to take your three Pre-Affine Transforms and move them so that they look like the image below: 

 ![](wing-Chaotica/WingShape.png)

 You will notice in the picture above that the white Reference Axis is four grid units tall and four grid units accross.  If your reference Axis is four units by four units, skip the rest of this paragraph.  If not, then right below the grid are two options called grid steps and grid spacing.  Set grid steps to 4 and grid spacing to .25.  ![](wing-Chaotica/GridSteps.png).  This will make your grid lines look like the ones above.  


You will want to shrink the red Pre-Affine Transform and move it below the white Reference Transform, and rotate it clockwise a little.  Then you will want to take the purple Pre-Affine Transform, shrink it a little, and move it directly to the left about half a grid unit.  And then you will want to take the blue Pre Affine Transform, shrink it by about half, move it up a hair over one unit, and move it over a hair under one unit, and rotate it.  

For this particular exercize, the closer you make your triangles look like the picture above, the more your fractal will look like a wing.  Precision counts.  In the next section, I will tell you how to type in the exact coordinates of each Pre-Affine Transform, but for the moment I want you to try moving the triangles around by hand.  Why?  Because this is one of my favorite parts of making a fractal: actually clicking on the triangles and seeing the fractal change on the main screen.  When I first started out, it gave me a godlike sense of power to be able to poke and prod the arrows and have something gorgeous show up, even if I had no idea what I was doing.   

After doing this, take a look at your main window.  How close to a wing shape did you get?  Don't worry if it's not exact, because, in the next section I'll tell you how to type in the exact coordinates.  Here's how the fractal looks on my screen after moving the Pre-Affine Transforms by hand.  

![](wing-Chaotica/ByHand.png)

Now is a good time to save your fractal, and a good time for me to explain the two different types of saving in the File menu.  If you go to the file menu, you'll see two save options:  Save World and Save Image, like below. 

![](wing-Chaotica/TwoSavingMethods.png)

You want to choose the Save World option.  Why?  Because Save World saves the formula used to make the fractal: all of the math and options and such.  It's basically a blueprint that Chaotica uses to rebuild the fractal if you open it again.  By contrast, Save Image just saves a picture of the fractal.  If you save an image and DON'T save the World too, you won't be able to reopen and edit the fractal in Chaotica.  You will know the hearbreak of many fractal artists who have pictures of fractals they've made, but didn't save the World.  Since they didn't save the world too, they'll probably never be able to make that fractal again.      

Saving the world gives you a file that ends in .chaos, like the following file: 

![](wing-Chaotica/ChaosFile.png)

Moving the Pre-Affine Transform with the Node Editor
----------------------------------------------------

Moving the transforms with the mouse is fun, but you can't get the transforms into exactly the same positions as shown in last section's picture.  To get exactly the same picture, you need to type the coordinates in by hand.  As a result, I'm going to teach you how to move the fractal with the Node Editor.  

First, click on the red Pre-Affine Transform.  You will notice, in the Iterators window, that the iterator named iter 0 is highlighted in orange.  

![](wing-Chaotica/Pre-AffineHighlighted.png)

Right below that, you will notice the Node Editor, which looks like this:  

![](wing-Chaotica/NodeEditor.png)

This is where you can enter precise coordinates to place your Pre-Affine Transform.  

Let's take a look at how these settings relate to the Pre-Affine Tranforms on the grid.
Let's look at the X axis of the Pre-Affine Transform.  
![](wing-Chaotica/Iter0XaxisVisual.png) ![](wing-Chaotica/Iter0Xaxis.png) 

I'll start with X-axis length, because it's pretty easy.  Length is how long the long shaft of the axis is.  

![](wing-Chaotica/Length.png)

Now let's deal with angle.  Let's pretend that the little circle on the X axis is the center of a clock, and that the X axis is the minute-hand on a clock.  Now imagine that the X axis is pointing at 15 minutes past the hour. When the X axis is pointed at fifteen minutes past the hour, it is horizontal. When the x axis is horizontal, it is at zero degrees.  Now, imagine that one minute passes, and the minute-hand  moves clockwise around our clock. The X axis is now at a slight angle to the horizon.  If we measure that angle, it's about six degrees.  It is negative six degrees because negative stands for both 'below the horizon' and 'clockwise' and positive stands for 'above the horizon' and 'go counterclockwise.'

![](wing-Chaotica/Angle.png)

If this is confusing to you, don't worry too much about it.  Just grab the arrowhead of the x axis, drag it around a little bit, and watch the numbers change until you get an intuition for it.  If you're like me, and you simply have to know what's going on here, google 'polar coordinates,' because having coordinates defined by a length and an angle are called polar cordinates.

The Y-axis coordinates work exactly the same as the X-axis coordinates. 

Now let's take a look at the last coordinate: Offset.

![](wing-Chaotica/Offset.png)

 The offset tells where on the grid the Pre-Affine Transform is in relation to the white reference transform.  For example, this one is a tenth of a unit to the left and one unit down from the white Reference Transform.  (For those who want more info, google 'cartesian coordinates').

 ![](wing-Chaotica/OffsetCoordinates.png)




Moving the Transform With the Transform Tab
-------------------------------------------

Moving transforms with the mouse is fun, but you can't get the
transforms into exactly the same positions as shown in last section's
picture. To get exactly the same position, you need to type the
locations in by hand. As a result, I'm going to teach you how to move
the fractal with the Transform tab.

### Transform Editor Tabs

Below the transform menu you will see a set of tabs.

![](wing/images/tabs.jpg)

Within these tabs you will find almost every option you need to control
how your fractal works. These tabs will look slightly different in
different versions of Apophysis, but as of this writing every version
has a Triangle tab, a Transform Tab, a Color tab, a Variations tab, and
a Variables tab. Some versions of Apophysis have a Xaos tab that is not
pictured here because I am using screenshots from an older version of
Apophysis. Future versions may have even more tabs as programmers decide
to add more features. In this particular tutorial we are only going to
talk about the Transform tab and the color tab.

### The Transform Tab

Click on the Transform tab ![](wing/images/transformtab.jpg). The
Transform tab will bring up a bunch of options shown below.

![](wing/images/transformtabopen.jpg)

The only options we care about for the moment are the top set of X, Y
and O options.

![](wing/images/transformtabXYO.jpg)

Here's where things begin to get a little tricky.

Select any transform. I'm going to select the first (red) transform, but
any of transform will work for this demonstration.

Notice that the transform has three points: O, X, and Y, and there are
three fields corresponding to each point.

![](wing/images/transformtabOXY.jpg)

Now for the slightly confusing part. The transform's O point is measured
from the Reference Transform's O point. So, in the picture below,
Transform 1's O point is -0.101175 units over from the reference
transform's O point and 0.979277 units up from the reference transform's
O point.

![](wing/images/transformOdistance.jpg)

So far so good. Let's take a look at the X and Y points. The X and Y
points are measured from the current transform's O point, NOT from the
reference triangle's O point. For example, the red transform's X point
is .595029 units over form the red transform's O point ant 0.055193
units up from the red transform's O point.

![](wing/images/transformXOdistance.jpg)

The Y point of the red transform is also measured from the red
transform's O point in exactly the same way as the X point.

![](wing/images/transformYOdistance.jpg)

All of this has an interesting effect. If you move the transform's O
point around on the screen, and watch the numbers in the boxes change in
the transform tab, only the values for the O point change.

So to use the transform tab value boxes keep in mind that the
transform's O point is measured from the reference transform's O point,
and the transform's X and Y points are measured from the transform's own
O point.

### Putting it all together

So, what does the transform tab give us, besides the chance to be really
confused? Well, it will let you make exactly the same wing I made in
this tutorial.

Select transform 1. ![](wing/images/transform1.jpg) and fill the
following values into the transform tab value boxes.

![](wing/images/transform1values.jpg)

Select transform 2 ![](wing/images/transform2.jpg) and fill in the
following values into transform 2's transform tab value boxes.

![](wing/images/transform2values.jpg)

Select transform 3 and fill in the following values into transform 3's
transform tab value boxes.

![](wing/images/transform3values.jpg)

Tada! You now have a wing shape!

Coloring Your Fractal
=====================

So now we have the shape of the fractal. Lets do something about the
color. There are two main ways of controlling the fractal's color in
Apophysis. The gradient controls what colors are used to color your
fractal, and the color tab in the transform editor controls how the
coloring is actually done. Right now I'm going to use whatever default
gradient was randomly applied to your fractal, and tell you how to
change it after we add more than one color to the fractal.

The Color Tab
-------------

You can color it lots of different ways, but I'll show you my favorite,
and in a later tutorial, I'll explain how the coloring actually works.
For now, in the Transform Editor, on the right-hand side, select the
Colors tab ![](wing/images/colortab.jpg).

![](wing/images/transformeditorcoloring.jpg)

Select transform 1, ![](wing/images/transform1.jpg). Put the color
slider all the way to the right. The value of the transform color will
show 1.000.

![](wing/images/transform1color.jpg)

Select transform 3, (the middle transform)
![](wing/images/transform3.jpg). Put the color slider all the way to the
right. The value of the transform color will show 1.000.

![](wing/images/transform3color.jpg)

Leave transform two's color slider alone, and voilà! We have my favorite
way of coloring a wing.

![](wing/images/coloredwing.jpg)

If you don't like this particular way of coloring, play around with the
sliders some more. For an explanation of why the fractals color the way
they do, look in a later chapter.

The Gradient Editor
-------------------

So, we now like the way the wing is colored, but what if we actually
want to change the colors?

It's time to look at the gradient editor. Quit out of the transform
editor and go back to the main apophysis window. Click on the gradient
button ![](wing/images/gradientbutton.jpg) . This will open up the
gradient editor, shown below. Technically, the window you open is called
the Adjust window and the gradient editor is the gradient tab within the
adjust window, but I like to call it the gradient editor because that's
what it is.

![](wing/images/colormenu.jpg)

In the Gradient Menu, you can see the Gradient, which shows you what
colors are being used to color your fractal.

![](wing/images/gradient.jpg)

You can also see the rotate slider. ![](wing/images/rotateslider.jpg) If
you move the slider, you can watch the order of the colors change on
your fractal.

![](wing/images/rotatedcolormenu.jpg)

But what if you want to completely change the color scheme? Then you
need to look at the presets menu. ![](wing/images/presetmenu.jpg) Click
on the arrow button ![](wing/images/dropdownarrow.jpg) to show the
gradients in the preset menu.

![](wing/images/presetmenudropdown.jpg)

I happen to like gradient 302 with a rotation of 72, so that's what I
will pick to color my wing.

I happen to like gradient 302 with a rotation of 72, so that's what I
will pick to color my wing.

![](wing/images/gradient302adjust.jpg)

And that gives me this beautiful wing!

![](wing/images/finalcoloredwing.jpg)

Rendering Your Fractal
======================

Now that you've made your fractal, you probably want to render it.

Framing your Fractal: Setting Up the Aspect Ratio
-------------------------------------------------

The first thing you'll want to do when setting up your fractal for
rendering is determine exactly what size of picture you want to render.
You'll then want the main window to show that size picture. This means
we have to play with something called the aspect ratio.

If you don't know what an aspect ratio is, it's how wide an image is
compared to how tall it is. In apophysis, we control the aspect ratio by
setting the width and height of an image in pixels.

So let's do exactly that.

In the main window, on the top menu, click on the Adjust button
![](wing/images/adjustbutton.jpg). The adjust menu will show up.

![](wing/images/cameratabadjustwindow.jpg)

Click on the Image Size tab ![](wing/images/imagesizetab.jpg) . The
image size dialog will show up.

![](wing/images/imagesizedialog.jpg)

Set width and the height of your image using the width and height box.

![](wing/images/widthandheight.jpg)

The width and height are in pixels. I set mine to 800 by 600, but you
can set yours to different values if you want.

If you notice that every time you change the width, your height changes
too, this is because the maintain aspect ratio box
![](wing/images/maintainaspectratio.jpg) is checked. The maintain aspect
ratio box makes sure that even if the size of the picture changes, the
proportion of with to height doesn't change. If you want to change the
height and width separately, uncheck the Maintain aspect ratio box.

The other thing on this dialog that you'll want to take a look at is the
Resize Main Window box. If you check this box, it will make sure that
the fractal image in your main window is resized to be exactly the same
size the final render will be. Click Apply to see the new frame for you
picture in the main window.

![](wing/images/resizemainwindow.jpg)

The big advantage of setting the aspect ratio in the image size tab is
that when you resize the main window, the preview window will still show
the right aspect ratio, so you will still have a good idea of what your
final picture is going to look like.

So, now that we know how to frame our image, let's see if we can't get
the wing to look a bit prettier inside that frame.

Moving the Fractal Inside the Frame
-----------------------------------

You may have noticed that while your wing is very pretty, it is also a
bit vertical. To show it off properly, it really needs to be horizontal.
There are two ways to do this

### Moving the with the Main Window

#### Rotation

Go to the main window.

![](wing/images/mainwindowfinalcolor.jpg)

Across the top you will see a menu.

![](wing/images/shortmenu.jpg)

This menu does not have what you want. This is because your window is
too small. Go to the lower right-hand corner of your window and use your
mouse to drag this corner ![](wing/images/dragcorner.jpg) until the rest
of the buttons appear across the top.

![](wing/images/menus.jpg)

To rotate your wing, you need to select the rotate button
![](wing/images/fractalrotatebutton.jpg)

In the fractal window of your main screen, click and drag with your
mouse. A rectangle outlined by a dotted line will show where your wing
is going to rotate to.

Let go of the mouse, and your fractal will show up rotated in a few
seconds.

![](wing/images/fractalrotated.jpg)

#### Translation

So what do you do if your wing looks a little off-center?

![](wing/images/offcenterwing.jpg)

In the main window, go up to the top menu and click on the Translate
Image button ![](wing/images/translateimagebutton.jpg).

Then, in the main window, click and hold with the mouse and start
dragging the image around until you have it where you want it, and let
go of the mouse.

#### Zooming

If you want to zoom in closer to your fractal, go to the main menu's top
menu bar and click on the zoom to rectangle button
![](wing/images/zoominbutton.jpg)

The zoom to rectangle button zooms by having you draw a rectangle around
the part you want to see and then matching the edges of the main window
as closely as possible to that rectangle.

To use the zoom to rectangle button, click and hold in the main window
where you want a corner of your selected rectangle to be, and then drag
the mouse to draw the rectangle.

![](wing/images/zoomtorectanglemain.jpg)

The main window will zoom in.

![](wing/images/zoomedmain.jpg)

The top menu bar's rectangle zoom out button
![](wing/images/zoomoutbutton.jpg) works like the rectangle zoom in
button, but in reverse. I'll leave that to you to play with.

I would like to point out that there are advantages and drawbacks to
this method of zooming. You can use this method to zoom in as far as you
want, but as you zoom in you'll notice that the image gets more noisy
and less well-defined.

![](wing/images/zoommaindemo.jpg)

This is because, in order to make a fractal image show up quickly on
your screen, the rectangle tool throws actual image quality out the
window. And most of the time, you don't need a really high quality image
to get an idea of what your fractal is going to look like. After you
render the fractal, all that noise is going to go away anyway.

There are ways to get a more high-quality zoom, but you'll read about
them in the next section.

### Move Your Fractal with the Camera menu

There is another, more precise way to rotate your fractal, and that is
by using the Camera tab of the adjust menu. In the main window on the
top menu bar click on the adjust button
![](wing/images/adjustbutton.jpg) .

It will bring up the adjust menu with the Camera tab already selected.

![](wing/images/cameratabadjustwindow.jpg)

To rotate your wing, simply move the Rotation slider, or type in the
exact degrees of rotation you want in the dialog beside the rotation
slider.

![](wing/images/cameratabrotationslider.jpg)

### Translating with the Camera Slider

You can move the fractal's position with the X position slider and the Y
position slider in the camera tab of the adjust menu.

![](wing/images/xandypositionslider.jpg)

However, there is a trick to using these sliders. See, these sliders
only work the way you think they would work if the rotation slider is
set to zero degrees of rotation. This is because the X axis is
horizontal and the Y axis is vertical when the rotation is 0.

![](wing/images/rotationslider0.jpg)

If you move the X slider, the wing moves left or right, and if you move
the Y slider, the wing moves up or down. Below is a picture of the
fractal with everything set to zero, and with a blue X axis and a red Y
axis drawn in. If you moved the sliders, those are the axises along
which the fractal would move. If you move the x slider, the picture
would move along the blue line. If you move the Y slider, the picture
would move along the red line.

![](wing/images/cameratab0.jpg)

However, if you move the rotation slider, the X and Y axis rotates as
well. That means that when you move the X slider, the fractal will still
move along the X axis, but since the X axis is rotated as well, your
fractal is probably going to move in a diagonal line across the screen.
Below is the fractal rotated 30 degrees. If you move the X slider, the
fractal will move along the blue diagonal line and if you move the Y
slider, the fractal will move along the red diagonal line.

![](wing/images/cameratab30.jpg)

As a result, I find it easier to move the fractal with the translate
image hand ![](wing/images/translateimagebutton.jpg) on the main screen.

### Zooming

In the camera tab of the adjust menu, you can also zoom in on the image
using the zoom slider. It will zoom in to wherever the center of the
picture is.

![](wing/images/zoomslider.jpg)

However, there are a couple of drawbacks to this method of zooming. The
more zoom you use, the longer it takes for the main window to render
your fractal. On a fast computer, it may take as much as five seconds.
On a slow computer, you could be waiting several minutes for it to
render the zoomed in fractal.

But wait (you might ask) why didn't you mention this problem when using
the rectangle zoom tool ![](wing/images/zoominbutton.jpg) on the main
screen? Well, the rectangle zoom tool does not have this problem. Why
not? Instead of answering, I'll show you a pair of pictures.

![](wing/images/zoommaindemo.jpg)

The above picture was done with Apophysis rectangle zoom

![](wing/images/zoomadjustdemo.jpg)

The above was done with the zoom slider on the camera tab of the adjust
window.

Compare the two pictures. Notice how the one done with the Rectangle
tool zoom is a lot grainier than the one done with the camera tab zoom.
That is why the Rectangle tool zoom is a lot faster than the camera tab
zoom- the rectangle tool sacrifices quality in order to get something up
very very fast. The zoom slider, on the other hand, gives you a good,
quality preview of the close-up, but because of the quality, displaying
that closeup is painfully slow.

You should also note that there is a limit to how far you can zoom in
with the zoom slider. You can only zoom in up to a certain, rather
arbitrary limit. With the Rectangle zoom too, there is no limitation to
how far you can zoom, except the practical limitation that the more you
zoom in, the less there is to see because of the sacrifices made for
fast rendering.

Rendering Your Fractal
----------------------

And now, all your hard work pays off, because we are now going to render
the fractal! In the main window in the top menu bar, click on the Render
button ![](wing/images/renderbutton.jpg). The Render Window will come
up.

![](wing/images/renderwindow.jpg)

### File Types and Saving Files

The first thing you need to do is set the Destination, which is where
your final rendered image will be saved.

![](wing/images/destinationpath.jpg)

Click on the file browser button. ![](wing/images/filebrowserbutton.jpg)
The file browser window will open.

![](wing/images/filebrowserwindow.jpg)

Browse around until you find a folder where you want to stash your
images.Then give your picture a name in the file name field.

![](wing/images/filenamefield.jpg)

Now take a look at the Files of type dropdown menu. You can render your
files as three different file types: a bitmap (.bmp) file, a PNG image
(.png), or a jpg image (.jpg)

The different file types do different things. Perhaps the most important
difference is the difference between the PNG format and the other two
formats.

The PNG format lets parts of the fractal be transparent. Specifically,
it lets you render the fractal on a transparent background, which is
very useful when you are going to be using the image together with
several other other images (i.e. compositing the images together.)

![](wing/images/wingtutorialcolored.png)

As you can see, the wing above lets the background show through.

By contrast, if you choose JPG for your encoding, the fractal will
render on whatever color background you have set. I haven't told you yet
how to set the background color, so for the moment you're probably
rendering on the default black background.

![](wing/images/wingtutorialcolored.jpg)

And that leaves us with the bitmap format. Hardly anybody uses the BMP
format, because the BMP format looks exactly like the .JPG format, and
has more disadvantages. The disadvantage of using .BMP is that there is
absolutely no compression on the image, so the file size is really
really big, which makes it hard to store a lot of images.

### Setting the Size

Now we get to determine the size of the image. By default, Apophysis
tries to render things at 1024 by 760, which is the standard default
resolution for computer displays. If you want the size settings to match
the settings you set in the image size tab of the Adjust menu, you need
to change them.

![](wing/images/imagesizerender.jpg)

Change the width to 800. If you have the maintain aspect ratio box
checked, the height will automatically change to 600. If you want to
change the height and weight separately, you'll need to uncheck the
maintain aspect ratio box.

The larger you make the image size, the longer it will take to render,
and the more memory you will need on your computer. The memory usage box
keeps track of how much memory you will need for a particular size
image, as well as for other setting's we'll get to in the next section.

![](wing/images/memoryusage.jpg)

If you make the image too big, however, you will run out of memory.

![](wing/images/memoryusage.jpg)

### Rendering options

Which brings us to the Rendering options. There are three rendering
options. Quality, Filter Radius, and Oversample.

![](wing/images/renderingoptions.jpg)

As a general rule of thumb, the higher these values are, the more higher
quality your fractal will be, and the more time it will take to render
the fractal. A higher quality tends to make the fractal more smooth and
less grainy, as does a higher oversample. I have no idea what the Filter
Radius does, because it has not been adequately explained to me yet.

For rendering the wing, the default settings will do.

### Clicking the Render Button

All that's left is to hit the Render button. So hit it!

![](wing/images/renderitbutton.jpg)

The rendering output window will show up, and give you information, a
progress bar, and an estimated time of how long it will take.

![](wing/images/rendering.jpg)

When it's done, you'll have your beautiful wing!

![](wing/images/wingtutorialcolored.jpg)

Wing Tutorial Resources
=======================

### A Brief Digression 

I'm going to chat for two paragraphs now about two different schools of thought there are in how to make fractals, so feel free to skip ahead.  The first school of thought are Explorers.  Explorers like to spend hours moving the transforms around, 'tweaking' the fractal here and there and trying things to see what happens.  Explorers usually have no idea how to make a particular fractal, just like an explorer often has no idea what will happen as they go into the great unknown.  Explorers don't know the theory or the math behind fractals, and don't care: they just want to poke around and see what happens.  These people are extremely valubale to the community because, over time, they get a sort of 'instinct' for fractals and can tell you how to make specific fractals, and what to do to get a particular effect. They also create entire libraries of fractals ans share them.  The second school of thought are the Engineers.  They want to take apart the fractal program and figure out HOW it does what it does, and why exactly putting a Pre-Affine transform in one location makes a tree while putting a Pre-Affine Transform in another location makes a wing.  They'll often study and research for weeks or even months before making a fractal, because they have a very particular fractal in mind that they want to make, and they need to know the math to make it.  Engineers like developing new types of fractals and making the programs the explorers use to make fractals. 

The two schools of thought combine to form the Chaotica fractal community. In general, the Engineers end up making new varieties of fractals, and give them to the Exporers.  The Exporers take the basic design and tweak it to come up with ever-more-spectacular fractals.  Both produce some spectacular work.  Being an Explorer takes a lot of patience and a willingness to create even when you have absolutely no idea what you are doing.  Being an engineer means being patient, being willing to wade through several thick textbooks, find scarce fractal-making resources, piecing together obscure bits of math and pestering fractal experts on how stuff works until you arrive at a sudden insight.  This is why fractal art is very popular, because the two methods play to the strengths of both artists who hate math and mathemeticans who woudn't know art if it bit them.  One of the things I love best about the fractal art community is that two groups of people who barely talk to eachother in real life chat back and forth and use their respective skills to make brilliant art.  

Now, back to making a wing.  Moving transforms by hand is called 'tweaking,' and it's the way 99% of fractal artists make new fractals.  You'll notice that moving the Pre-Affine transform changes the shape of the fractal in mysterious and beautiful ways.  Many artists spend hours tweaking the transforms just to see what happens, and if you're inspired to do so, I highly encourage you to spend some time twirlings stuff.  Make sure you save your result, though.  One thing about fractals is that, unless you write exactly waht you did or save your work, you will never see that fractal again.  


The parameters for the wing in various stages of construction can be
found [here](wing/wingtutorial.flame)
