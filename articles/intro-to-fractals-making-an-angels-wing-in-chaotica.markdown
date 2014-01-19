Title: Intro To Fractals: Making An Angel's Wing using Chaotica
Author: Tara Roys
Date: Wed Sept 27 2013 10:16:51 GMT-0600 (CST)
Node: v0.1.102

Introduction
============

![](wing-Chaotica/RainbowWingFinal.png)

This tutorial assumes you have zero knowledge of fractals or of Chaotica.

You can use Chaotica with any operating system.  The latest version of Chaotica can be downloaded from [the Chaotica Website.](http://chaoticafractals.com/)

This chapter will teach you how to make the fractal wing shown above. By the end, you will know how to use the most important parts of the Chaotica user interface, and you will have a lovely picture to show to your friends.  

This tutorial will tell you how to make a wing.  It will NOT explain the principles behind fractals or Chaotica.  Think of it like a cook-book recipe: a recipe tells you how to make a loaf of bread, but it does not tell you about the science behind bread-making.


The Main Screen
===============

This tutorial is a general introduction to Chaotica. It introduces all of the important aspects of the program's user interface.

![](wing-Chaotica/parameterbrowser.png)

First, open Chaotica. In a window called the "parameter browser," you will see nine colorful fractals like the ones above.  They will not be exactly like the ones shown here. Click on one that you like, and close the parameter browser.

![](wing-Chaotica/chaoticamain.png)

You will now see the main screen, as shown above.  There are lots of options on the main screen. At the moment, we only care about one option: AA Level.

![](wing-Chaotica/AALevel.png)

On the left-hand side of the screen, you will see an option called AA Level in the "Resolutions and Channels" section. (It is highlighted in orange in the image above.) Set it to 1. This makes the program draw the fractal faster. 

![](wing-Chaotica/mainmenu.png)

Turn your attention to the main menu, shown above.    

![](wing-Chaotica/openWorldEditor.png)

In the main menu, click on Window and then World Editor to open the World Editor. 



Moving Your Fractal: The World Editor
=========================================

![](wing-Chaotica/WorldEditor.png)

This is the World Editor.  This is where you can change the shape of your fractal. You will learn to love the World Editor, because this is where you will spend most of your time.



Moving around in the World Editor
-------------------------------------

![](wing-Chaotica/blackgrid.png)

When you open the world editor, the first thing you'll see is a large black screen with a bunch of angles and a grid on it. The first thing to learn is how to move around in this window.

Right-click and hold on the black grid.  While still holding the right mouse button down, move the mouse around. You'll drag the grid around. This lets you reposition your editor window so that you can concentrate on whatever part you want.

To zoom in and out of the editor window, hold down ALT and the right mouse button, then drag the mouse around. Dragging the mouse up will zoom in, whereas dragging the mouse down will zoom out.  

Making a New Flame
------------------

You'll notice that the picture above has a lot of colored angles pointing in different directions. When you click on one of the arrows and drag it around, you'll notice that you change how the fractal looks. 

Delete all but one set of angles and start over.  You can do it by hand. Here's how to do it by hand. 

![](wing-Chaotica/delete_iterator.png)

In the iterators window, click on an iterator, such as "Iterator 2" shown in the picture above. Then press the delete button.  One of the angles will disappear.  Do that until only one angle remains.  Chaotica will not allow you to delete the last angle, because you cannot make a fractal without at least one angle. 

![](wing-Chaotica/select_angle.png)

Note: Many people try to select an angle on the black screen and press delete.  This does not work.  Why?

![](wing-Chaotica/select_angle_iterator_window.png)

If you notice the iterator window, you will notice that something called the Pre-Affine is highlighted orange, NOT the iterator itself. To be very brief, a fractal is made of parts called iterators. An iterator has many parts. A Pre-affine (which is short for "Pre-Affine Transform") is merely a part of an iterator, not the whole iterator. The angles are a visual representation of the Pre-Affine.  Trying to delete just the pre-affine is like trying to throw away just a page of a book and thinking that the page is the whole book.  That's why you can't delete by hand just by selecting an angle on the black grid.




 but to get on with actually making the wing and skipping a lot of the boring setup, do the following.  Copy all of the code in the black box below.  

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

Now we can start building a wing!



### Moving a Pre-Affine Transform With The Mouse

Go to the world editor where you'll find the following:

![](wing-Chaotica/BlankFlameIterator.png)

Click on the red thing that looks like a pair of arrows coming out from a point.  That thing is called a Pre-Affine Transform. 

 Note: Some like to shorten it and call it a "Transform" because "Pre-Affine Transform" sounds long and scary.  However, for the rest of the tutorial, its called by its full name: Pre-Affine Transform. Why? Because there are six different things in Chaotica labeled "Transform," and you won't get confused about which one is which. Don't worry about the scary-sounding name for now.  

Click on it.  You should see two things.  First, the Pre-Affine Transform is highlighted on the grid, like so: 

![](wing-Chaotica/Pre-AffineTransformHilighted.png)

Second, you will see the name pre-affine higlighted in orange in the iterators panel in the upper-right-hand corner of the world editor, like so:  

![](wing-Chaotica/Pre-AffineHilighted.png)


Let's get this thing moving!

If you've ever worked with Photoshop or a similar image editor, you know that you can move an image in several different ways. In the picture below  the green shape is the original shape, and the yellow shape is moved in some way.  Each particular type of movement has its very own fancy technical term that sounds all scary and strange, but really, they're just names for the very ordinary sorts of movements you'd want to do to a picture.  

  

![](wing-Chaotica/AffineTransform.png)

Taken together, these five movements are called Affine Tranformations, which is where the 'Affine' part of 'Pre-Affine Transform' comes from.  Let's learn how to do these five movements to our pre-affine transform.  

Disclaimer:  the following section talks a little bit about math; however, the math described here is a lot like a stick figure.  You can communicate a lot of information with a stick figure, but nobody is going to mistake it for a realistic drawing. Like a stick figure, the math described in this section is wildly oversimplified, and the technical terms used in it are a bit inaccurate.  So, math people, if I'm making your teeth grind together, there's a paragraph at the end of this section full of links to much more accurate and much less readable information just for you.  

### Translation

Look at the Pre-Affine Transform. Notice that they are made of two arrows. In math terms, an arrow is called an 'axis.'  I am going to use the term 'axis' instead of 'arrows' for the rest of the tutorial. 

Look at where the two axes meet.  There is a small circle that looks like this: 

![](wing-Chaotica/origin.png)

This circle is called the origin.  Click and drag it.  

Clicking and dragging on the origin allows you to translate the Pre-Affine Transform.  

Now is a good time to point out the white axes.  The white axes are the Reference Axes that tell you how far away from the center of the picture you have moved your Pre-Affine Transform.

![](wing-Chaotica/Translation.png)

In this picture, the Pre-Affine Transform has been moved down and to the left of the Reference Axes.  

### Rotation

Look at the Pre-Affine Transform. See how each axis is made of a circle, a long line, and an arrowhead.  Click and hold on the long line, as shown below, and drag the mouse.  


![](wing-Chaotica/Rotation.png)

This will rotate the Pre-Affine Transform.  

### Scale

Notice the box that shows up around the Pre-Affine Transform when you click on it.  Move the mouse to one of the corners of that box.  While clicking and holding your mouse, drag the corner around. The Pre-Affine Transform will get bigger or smaller.  


![](wing-Chaotica/Scale.png)

### Skew  

Now look at the arrowhead at the top of the Y axis. (The Y axis is the axis with a y by it.)  Click and hold and drag it around.  This skews the Pre-Affine Transform, as shown below.  

![](wing-Chaotica/Skew.png)


### Reflection


There isn't actually a separate reflection widget in Chaotica.  However, you can drag the arrowhead of an axis so that it is on the opposite side from where it started.  

![](wing-Chaotica/Reflection.png)
Now that you know how to move one Pre-Affine Transform, play with a few more Pre-Affine Transforms.

If you want to know more about Pre-Affine Transforms, check out [the Wikipedia Page.](http://en.wikipedia.org/wiki/Iterated_function_system ) If you want to read an extremely dense math paper about how chaotica-type fractals are made, read [Scott Drave's paper on Iterated Function Systems.](http://flam3.com/flame.pdf) I don't recommend them for beginners, because at this point you probably don't care.  Let's move along.   

### Adding More Iterators

In the top left corner of the World Editor is a button called New Iterator. It looks like this:  ![](wing-Chaotica/NewIteratorButton.png)

Press it twice to add two new Iterators to your World Editor.  

Note: Iterators are the workhorses that generate the fractal.  What is the difference between a Pre-Affine Transform and an Iterator?  The Pre-Affine Transform that we're talking about is a part of the Iterator, in the same sense that a spark plug is part of a car.  

Now that there are three iterators, start moving them around so that they form a wing shape.

### Creating the Wing Shape

In order to make a fractal that looks like a wing, you need to take your three Pre-Affine Transforms and move them so that they look like the image below: 

 ![](wing-Chaotica/WingShape.png)

 You will notice in the picture above that the white Reference Axis is four grid units tall and four grid units accross.  If your reference Axis is four units by four units, skip the rest of this paragraph.  If not, then right below the grid are two options called grid steps and grid spacing.  Set grid steps to 4. ![](wing-Chaotica/GridSteps.png).  This will make your grid lines look like the ones above.  

Shrink the red Pre-Affine Transform and move it below the white Reference Transform, and rotate it clockwise a little.  Then take the purple Pre-Affine Transform, shrink it a little, and move it directly to the left about half a grid unit.  And then take the blue Pre-Affine Transform, shrink it by about half, move it up a hair over one unit, and move it over a hair under one unit, and rotate it.  

For this particular step, the closer you make your Pre_Affine Transforms look like the picture above, the more your fractal will look like a wing.  Precision counts.  In the next section, you will learn how to type in the exact coordinates of each Pre-Affine Transform, but for the moment try moving the Pre-Affine Transforms around by hand.  Why?  Because this is one of my favorite parts of making a fractal: actually clicking on the triangles and seeing the fractal change on the main screen.  When I first started out, it gave me a godlike sense of power to be able to poke and prod the arrows and have something gorgeous show up, even if I had no idea what I was doing.   

After doing this, take a look at your main window.  How close to a wing shape did you get?  Don't worry if it's not exact, because, in the next section you'll learn how to type in the exact coordinates.  Here's how the fractal looks on my screen after moving the Pre-Affine Transforms by hand.  

![](wing-Chaotica/ByHand.png)

Now is a good time to save your fractal, and a good time for me to explain the two different types of saving in the File menu.  If you go to the file menu, you'll see two save options:  Save World and Save Image, like below. 

![](wing-Chaotica/TwoSavingMethods.png)
Choose the Save World option.  Why?  Because Save World saves the settings used to make the fractal.  It's basically a blueprint that Chaotica uses to rebuild the fractal if you open it again.  By contrast, Save Image just saves a picture of the fractal.  If you save an image and DON'T save the World too, you won't be able to reopen and edit the fractal in Chaotica.  You will know the heartbreak of many fractal artists who have pictures of fractals they've made, but didn't save the World.  Since they didn't save the World too, they'll probably never be able to make that fractal again.      

Saving the world gives you a file that ends in .chaos, like the following file: 

![](wing-Chaotica/ChaosFile.png)

Moving the Pre-Affine Transform with the Node Editor
----------------------------------------------------

Moving the transforms with the mouse is fun, but you can't get the transforms into exactly the same positions as shown in last section's picture.  To get exactly the same picture, you need to type the coordinates in by hand. Here'show to move the fractal with the Node Editor.  

First, click on the red Pre-Affine Transform.  Notice, in the Iterators window, that the iterator named iter 0 is highlighted in orange.  

![](wing-Chaotica/Pre-AffineHighlighted.png)

Right below that, notice the Node Editor, which looks like this:  

![](wing-Chaotica/NodeEditor.png)

This is where you can enter precise coordinates to place your Pre-Affine Transform.  

Let's see how these settings relate to the Pre-Affine Tranforms on the grid.
Look at the X axis of the Pre-Affine Transform.  
![](wing-Chaotica/Iter0XaxisVisual.png) ![](wing-Chaotica/Iter0Xaxis.png) 

Start with X-axis length because it's the easiest.  Length is how long the long shaft of the axis is.  

![](wing-Chaotica/Length.png)

Now let's work with angle. Pretend that the little circle on the X axis is the center of a clock.  Then pretend that the X axis is the minute-hand on a clock.  Now, imagine that the X axis is pointing at 15 minutes past the hour. When the X axis is pointed at 15 minutes past the hour, it is horizontal. When the x axis is horizontal, it is at zero degrees.

Now, imagine that one minute passes, and the minute-hand  moves clockwise around our clock. The X axis is now at a slight angle. It is no longer horizontal. In fact, the angle between the X axis and a horizontal line is negative six degrees.

Why is it negative six degrees? It is negative six degrees because negative stands for 'going clockwise'.  If you changed the number to negative ten instead of negative six, you would see that the X axis rotated clockwise.  If you want the X axis to rotate clockwise, you would tell it to go 6 degrees.  In short, positive means rotating counterclockwise, and negative means rotating clockwise.  

![](wing-Chaotica/Angle.png)

If this is confusing to you, don't worry much about it.  Just grab the arrowhead of the x axis, drag it around a little bit, and watch the numbers change until you get an intuition for it.  (If you're like me, and you simply have to know what's going on here, google "polar coordinates," because having coordinates defined by a length and an angle are called polar coordinates.)

The Y-axis coordinates work exactly the same as the X-axis coordinates. 

Now let's take a look at the last coordinate: Offset.

![](wing-Chaotica/Offset.png)

 The offset tells where on the grid the Pre-Affine Transform is in relation to the white reference transform.  For example, the red transform is a tenth of a unit to the left and one unit down from the white Reference Transform.  (For those who want more info, google 'cartesian coordinates").

 ![](wing-Chaotica/OffsetCoordinates.png)

 Fortunately you don't have to understand polar coordinates or cartesian coordinates to be able to use the node editor. How it works is something you can pick up with a little experimentation.  

 Now that you know the basics of how the node editor works, we're going to use it to move the Pre-Affine Transform into exactly the positions I have them in.  

 Click on the red Pre Affine Transform.  Type in the numbers you see below exactly as you see them.  

  ![](wing-Chaotica/Iter0PreAffineNode.png)

 Click on the blue Pre-Affine Transform.  Type in the numbers you see below.  

  ![](wing-Chaotica/Iter1PreAffineNode.png)

 Click on the purple Pre-Affine Transform.  Type in the numbers you see below.  

  ![](wing-Chaotica/Iter2PreAffineNode.png)

At this point, if you go back to the main window, your wing should look like this: 

  ![](wing-Chaotica/WingShape2.png)

If you're having trouble with this, here is the source code for this step of the flame.  

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
          <int name="image_layers">1</int>
          <string name="antialiasing_mode">strong</string>
          <real name="brightness">4</real>
          <vec4 name="background_colour">0.1 0.1 0.1 1</vec4>
          <real name="flam3_gamma">3.6</real>
          <real name="flam3_vibrancy">1</real>
          <bool name="flam3_use_highlight_power">false</bool>
          <real name="flam3_highlight_power">0.003</real>
          <real name="flam3_gamma_linear_threshold">0</real>
          <table name="layer_weights">
            <values>1 1 1 1</values>
          </table>
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
          <iterator name="iter 0">
            <flam3_transform name="flam3_xform 0">
              <affine2 name="Pre affine">
                <real name="x_axis_angle">-5.2994108215588875</real>
                <real name="x_axis_length">0.5975832813006067</real>
                <real name="y_axis_angle">84.70058917844112</real>
                <real name="y_axis_length">0.5975832813006067</real>
                <vec2 name="offset">-0.101175 -0.979277</vec2>
              </affine2>
              <node name="transforms">
                <transform name="Transform 2">
                  <string name="type_name">linear3D</string>
                  <params>
                    <real name="linear3D">1</real>
                  </params>
                </transform>
              </node>
            </flam3_transform>
            <flam3_shader name="flam3 shader">
              <real name="palette_index">1</real>
              <real name="blend_speed">0.5</real>
              <real name="opacity">1</real>
              <table name="layer_weights">
                <values>1 1 1 1</values>
              </table>
            </flam3_shader>
            <weights_selector name="weights">
              <real name="base_weight">0.5</real>
              <node name="per_iterator_weights">
                <real name="iter 0 weight">1</real>
                <real name="iter 1 weight">1</real>
                <real name="iter 2 weight">1</real>
              </node>
            </weights_selector>
          </iterator>
          <iterator name="iter 1">
            <flam3_transform name="flam3_xform 1">
              <affine2 name="Pre affine">
                <real name="x_axis_angle">17.467311110854343</real>
                <real name="x_axis_length">0.4175383808298346</real>
                <real name="y_axis_angle">107.46731111085435</real>
                <real name="y_axis_length">0.4175383808298346</real>
                <vec2 name="offset">-0.219659 0.299224</vec2>
              </affine2>
              <node name="transforms">
                <transform name="Transform 2">
                  <string name="type_name">linear3D</string>
                  <params>
                    <real name="linear3D">1</real>
                  </params>
                </transform>
              </node>
            </flam3_transform>
            <flam3_shader name="flam3 shader">
              <real name="palette_index">1</real>
              <real name="blend_speed">0.5</real>
              <real name="opacity">1</real>
              <table name="layer_weights">
                <values>1 1 1 1</values>
              </table>
            </flam3_shader>
            <weights_selector name="weights">
              <real name="base_weight">0.5</real>
              <node name="per_iterator_weights">
                <real name="iter 0 weight">1</real>
                <real name="iter 1 weight">1</real>
                <real name="iter 2 weight">1</real>
              </node>
            </weights_selector>
          </iterator>
          <iterator name="iter 2">
            <flam3_transform name="flam3_xform 2">
              <affine2 name="Pre affine">
                <real name="x_axis_angle">-19.362429724905475</real>
                <real name="x_axis_length">0.830946093763007</real>
                <real name="y_axis_angle">77.39553838405824</real>
                <real name="y_axis_length">0.7557353951880248</real>
                <vec2 name="offset">-0.191135 -0.009043</vec2>
              </affine2>
              <node name="transforms">
                <transform name="Transform 2">
                  <string name="type_name">linear3D</string>
                  <params>
                    <real name="linear3D">1</real>
                  </params>
                </transform>
              </node>
            </flam3_transform>
            <flam3_shader name="flam3 shader">
              <real name="palette_index">1</real>
              <real name="blend_speed">0.5</real>
              <real name="opacity">1</real>
              <table name="layer_weights">
                <values>1 1 1 1</values>
              </table>
            </flam3_shader>
            <weights_selector name="weights">
              <real name="base_weight">0.5</real>
              <node name="per_iterator_weights">
                <real name="iter 0 weight">1</real>
                <real name="iter 1 weight">1</real>
                <real name="iter 2 weight">1</real>
              </node>
            </weights_selector>
          </iterator>
        </node>
      </flam3_IFS>

Coloring Your Wing
------------------

Now let's give this wing some color.  

Now, to get exactly the colors I am going to get, you need to copy and paste the following XML into Chaotica.  If you don't, you will get a pretty wing, but you won't get exactly the same the colors I have. 

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
        <int name="image_layers">1</int>
        <string name="antialiasing_mode">strong</string>
        <real name="brightness">4</real>
        <vec4 name="background_colour">0.1 0.1 0.1 1</vec4>
        <real name="flam3_gamma">3.6</real>
        <real name="flam3_vibrancy">1</real>
        <bool name="flam3_use_highlight_power">false</bool>
        <real name="flam3_highlight_power">0.003</real>
        <real name="flam3_gamma_linear_threshold">0</real>
        <table name="layer_weights">
          <values>1 1 1 1</values>
        </table>
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
        <iterator name="iter 0">
          <flam3_transform name="flam3_xform 0">
            <affine2 name="Pre affine">
              <real name="x_axis_angle">-5.2994108215588875</real>
              <real name="x_axis_length">0.5975832813006067</real>
              <real name="y_axis_angle">84.70058917844112</real>
              <real name="y_axis_length">0.5975832813006067</real>
              <vec2 name="offset">-0.101175 -0.979277</vec2>
            </affine2>
            <node name="transforms">
              <transform name="Transform 2">
                <string name="type_name">linear3D</string>
                <params>
                  <real name="linear3D">1</real>
                </params>
              </transform>
            </node>
          </flam3_transform>
          <flam3_shader name="flam3 shader">
            <real name="palette_index">1</real>
            <real name="blend_speed">0.5</real>
            <real name="opacity">1</real>
            <table name="layer_weights">
              <values>1 1 1 1</values>
            </table>
          </flam3_shader>
          <weights_selector name="weights">
            <real name="base_weight">0.5</real>
            <node name="per_iterator_weights">
              <real name="iter 0 weight">1</real>
              <real name="iter 1 weight">1</real>
              <real name="iter 2 weight">1</real>
            </node>
          </weights_selector>
        </iterator>
        <iterator name="iter 1">
          <flam3_transform name="flam3_xform 1">
            <affine2 name="Pre affine">
              <real name="x_axis_angle">17.467311110854343</real>
              <real name="x_axis_length">0.4175383808298346</real>
              <real name="y_axis_angle">107.46731111085435</real>
              <real name="y_axis_length">0.4175383808298346</real>
              <vec2 name="offset">-0.219659 0.299224</vec2>
            </affine2>
            <node name="transforms">
              <transform name="Transform 2">
                <string name="type_name">linear3D</string>
                <params>
                  <real name="linear3D">1</real>
                </params>
              </transform>
            </node>
          </flam3_transform>
          <flam3_shader name="flam3 shader">
            <real name="palette_index">1</real>
            <real name="blend_speed">0.5</real>
            <real name="opacity">1</real>
            <table name="layer_weights">
              <values>1 1 1 1</values>
            </table>
          </flam3_shader>
          <weights_selector name="weights">
            <real name="base_weight">0.5</real>
            <node name="per_iterator_weights">
              <real name="iter 0 weight">1</real>
              <real name="iter 1 weight">1</real>
              <real name="iter 2 weight">1</real>
            </node>
          </weights_selector>
        </iterator>
        <iterator name="iter 2">
          <flam3_transform name="flam3_xform 2">
            <affine2 name="Pre affine">
              <real name="x_axis_angle">-19.362429724905475</real>
              <real name="x_axis_length">0.830946093763007</real>
              <real name="y_axis_angle">77.39553838405824</real>
              <real name="y_axis_length">0.7557353951880248</real>
              <vec2 name="offset">-0.191135 -0.009043</vec2>
            </affine2>
            <node name="transforms">
              <transform name="Transform 2">
                <string name="type_name">linear3D</string>
                <params>
                  <real name="linear3D">1</real>
                </params>
              </transform>
            </node>
          </flam3_transform>
          <flam3_shader name="flam3 shader">
            <real name="palette_index">1</real>
            <real name="blend_speed">0.5</real>
            <real name="opacity">1</real>
            <table name="layer_weights">
              <values>1 1 1 1</values>
            </table>
          </flam3_shader>
          <weights_selector name="weights">
            <real name="base_weight">0.5</real>
            <node name="per_iterator_weights">
              <real name="iter 0 weight">1</real>
              <real name="iter 1 weight">1</real>
              <real name="iter 2 weight">1</real>
            </node>
          </weights_selector>
        </iterator>
      </node>
    </flam3_IFS>


Click on the blue pre-affine transform.  In the Iterators window, under iter1, click on the Flame3 shader.  


  ![](wing-Chaotica/ColorIter1.png)


Below the Iterators, you will see a bunch of options.  Change the option called Palette Index to 0.  


  ![](wing-Chaotica/PaletteIndex.png)

In the main window, your wing will now look like this:  

  ![](wing-Chaotica/RainbowWing.png)

You can change the palette index on other Iterators as well, but this is my favorite way to color fractals.  I will explain why changing these values has the effect it has in a later tutorial.  

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
        <int name="image_layers">1</int>
        <string name="antialiasing_mode">strong</string>
        <real name="brightness">4</real>
        <vec4 name="background_colour">0.1 0.1 0.1 1</vec4>
        <real name="flam3_gamma">3.6</real>
        <real name="flam3_vibrancy">1</real>
        <bool name="flam3_use_highlight_power">false</bool>
        <real name="flam3_highlight_power">0.003</real>
        <real name="flam3_gamma_linear_threshold">0</real>
        <table name="layer_weights">
          <values>1 1 1 1</values>
        </table>
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
        <iterator name="iter 0">
          <flam3_transform name="flam3_xform 0">
            <affine2 name="Pre affine">
              <real name="x_axis_angle">-5.2994108215588875</real>
              <real name="x_axis_length">0.5975832813006067</real>
              <real name="y_axis_angle">84.70058917844112</real>
              <real name="y_axis_length">0.5975832813006067</real>
              <vec2 name="offset">-0.101175 -0.979277</vec2>
            </affine2>
            <node name="transforms">
              <transform name="Transform 2">
                <string name="type_name">linear3D</string>
                <params>
                  <real name="linear3D">1</real>
                </params>
              </transform>
            </node>
          </flam3_transform>
          <flam3_shader name="flam3 shader">
            <real name="palette_index">1</real>
            <real name="blend_speed">0.5</real>
            <real name="opacity">1</real>
            <table name="layer_weights">
              <values>1 1 1 1</values>
            </table>
          </flam3_shader>
          <weights_selector name="weights">
            <real name="base_weight">0.5</real>
            <node name="per_iterator_weights">
              <real name="iter 0 weight">1</real>
              <real name="iter 1 weight">1</real>
              <real name="iter 2 weight">1</real>
            </node>
          </weights_selector>
        </iterator>
        <iterator name="iter 1">
          <flam3_transform name="flam3_xform 1">
            <affine2 name="Pre affine">
              <real name="x_axis_angle">17.467311110854343</real>
              <real name="x_axis_length">0.4175383808298346</real>
              <real name="y_axis_angle">107.46731111085435</real>
              <real name="y_axis_length">0.4175383808298346</real>
              <vec2 name="offset">-0.219659 0.299224</vec2>
            </affine2>
            <node name="transforms">
              <transform name="Transform 2">
                <string name="type_name">linear3D</string>
                <params>
                  <real name="linear3D">1</real>
                </params>
              </transform>
            </node>
          </flam3_transform>
          <flam3_shader name="flam3 shader">
            <real name="palette_index">0</real>
            <real name="blend_speed">0.5</real>
            <real name="opacity">1</real>
            <table name="layer_weights">
              <values>1 1 1 1</values>
            </table>
          </flam3_shader>
          <weights_selector name="weights">
            <real name="base_weight">0.5</real>
            <node name="per_iterator_weights">
              <real name="iter 0 weight">1</real>
              <real name="iter 1 weight">1</real>
              <real name="iter 2 weight">1</real>
            </node>
          </weights_selector>
        </iterator>
        <iterator name="iter 2">
          <flam3_transform name="flam3_xform 2">
            <affine2 name="Pre affine">
              <real name="x_axis_angle">-19.362429724905475</real>
              <real name="x_axis_length">0.830946093763007</real>
              <real name="y_axis_angle">77.39553838405824</real>
              <real name="y_axis_length">0.7557353951880248</real>
              <vec2 name="offset">-0.191135 -0.009043</vec2>
            </affine2>
            <node name="transforms">
              <transform name="Transform 2">
                <string name="type_name">linear3D</string>
                <params>
                  <real name="linear3D">1</real>
                </params>
              </transform>
            </node>
          </flam3_transform>
          <flam3_shader name="flam3 shader">
            <real name="palette_index">1</real>
            <real name="blend_speed">0.5</real>
            <real name="opacity">1</real>
            <table name="layer_weights">
              <values>1 1 1 1</values>
            </table>
          </flam3_shader>
          <weights_selector name="weights">
            <real name="base_weight">0.5</real>
            <node name="per_iterator_weights">
              <real name="iter 0 weight">1</real>
              <real name="iter 1 weight">1</real>
              <real name="iter 2 weight">1</real>
            </node>
          </weights_selector>
        </iterator>
      </node>
    </flam3_IFS>


###Changing the Palette

I like this rainbow palette, but other people like different palettes.  To change the color, you can open the Palette Editor. Go to Window and click Palette Editor.  

![](wing-Chaotica/WindowPaletteEditor.png)

The Palette Editor will open. It looks like this:  

![](wing-Chaotica/PaletteEditor.png)

I don't know how the Palette Editor works, so what I do is press random things until I get a color pattern I like.  Feel free to do the same.  

Rendering Your Fractal
======================

Now that you've made your fractal, you probably want to render it.

Framing your Fractal: Setting Up the Aspect Ratio
-------------------------------------------------

The first thing to do when setting up your fractal for rendering is to determine exactly what size of picture you want to render.
You'll want the main window to show that size picture. This means you have to play with something called the aspect ratio.

If you don't know what an aspect ratio is, it's how wide an image is compared to how tall it is. In Chaotica, control the aspect ratio by
setting the width and height of an image in pixels.  

So let's do exactly that.

In the main window, on the left-hand side, there is a block called Render Settings.  It looks like this: 

    ![](wing-Chaotica/RenderSettings.png)

The Aspect Ratio is controlled by the Width and Height settings. The width and the height is in pixels.  I set mine to 800 by 600, but you can set yours to different values if you like.  

    ![](wing-Chaotica/AspectRatio.png)

If you notice that every time you change the width, your height changes
too, this is because the Lock Aspect Ratio box
 ![](wing-Chaotica/LockAspectRatio.png) is checked. The Lock Aspect
Ratio box makes sure that even if the size of the picture changes, the proportion of width to height doesn't change. If you want to change the height and width separately, uncheck the Lock Aspect Ratio box.


So, now that we know how to frame our image, let's see if we can't get the wing to fit a bit better inside that frame.

Moving the Fractal Inside the Frame
-----------------------------------

You may have noticed that while your wing is very pretty, it is also a
bit vertical. To show it off properly, it really needs to be horizontal. So let's rotate our wing.  Open the World Editor.  In the bottom right-hand corner are a bunch of settings called Camera Settings.  

![](wing-Chaotica/CameraSettings.png)

To center and re-orient your fractal, type in the settings shown above into your Camera Settings block.  Your wing will now look like this:  

![](wing-Chaotica/MainWindowReadyToRender.png)

##How Rendering Works:  

Here's the interesting and most powerful feature of Chaotica:  it is already rendering your fractal.  At the bottom of the main screen you will see a bunch of information that looks like this:  

![](wing-Chaotica/MainWindowRenderingInfo.png)

You may or may not have noticed that if you leave the main window alone for awhile, the fractal slowly goes from looking to a bit spotty to looking nice and smooth and bright.

The thing about fractals is that they take a computer a pretty long time to make. Imagine you are building a house, and you've drawn up a really good set of blueprints.  You take the blueprints and give them to the builder.  The builder is not going to be able to make the house magically appear in the next second.  It takes days or sometimes months to build a house.  

The same holds true of fractals.  What you have done up to this point is make a blueprint for a fractal. Now you are handing it to the computer and telling the computer, "Build me this fractal."

The nice thing about Chaotica is that you get to see the process as it happens.  The fractal goes from being a scaffold to a full fledged wing, and all you have to do is wait for awhile. 

How long should you wait?  The rule of thumb is to wait until you think it looks good.  Chaotica will keep rendering the fractal until you tell it to stop, so you can walk away from the computer and check up a few hours later and see if you think it is done.  A lot of people call this "putting a fractal on to cook."  

This fractal cooks pretty quickly. On my computer it takes about ten minutes before I consider it "done."

When it is done, go to File and select "Save Image."

![](wing-Chaotica/SaveImage.png)

Tada!  You now have a lovely new fractal!  

![](wing-Chaotica/RainbowWingFinal.png)

Here is the source code for this final wing.  
  
    <flam3_IFS name="New Blank Flame">
    <camera>
      <vec4 name="pos">-0.75 -0.5 0 1</vec4>
      <vec2 name="rotate">-75 -75</vec2>
      <real name="scale">400</real>
    </camera>
    <imaging name="Imaging">
      <int name="image_width">800</int>
      <int name="image_height">600</int>
      <int name="image_supersample">2</int>
      <int name="image_layers">1</int>
      <string name="antialiasing_mode">strong</string>
      <real name="brightness">4</real>
      <vec4 name="background_colour">0.1 0.1 0.1 1</vec4>
      <real name="flam3_gamma">3.6</real>
      <real name="flam3_vibrancy">1</real>
      <bool name="flam3_use_highlight_power">false</bool>
      <real name="flam3_highlight_power">0.003</real>
      <real name="flam3_gamma_linear_threshold">0</real>
      <curves>
        <curve name="overall">
          <table>
            <values>0 0.75 1 0.44949496 0.24242425</values>
          </table>
          <table>
            <values>0 0.75 1 0.4848485 0.25757578</values>
          </table>
        </curve>
      </curves>
      <table name="layer_weights">
        <values>1 1 1 1</values>
      </table>
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
      <iterator name="iter 0">
        <flam3_transform name="flam3_xform 0">
          <affine2 name="Pre affine">
            <real name="x_axis_angle">-5.2994108215588875</real>
            <real name="x_axis_length">0.5975832813006067</real>
            <real name="y_axis_angle">84.70058917844112</real>
            <real name="y_axis_length">0.5975832813006067</real>
            <vec2 name="offset">-0.101175 -0.979277</vec2>
          </affine2>
          <node name="transforms">
            <transform name="Transform 2">
              <string name="type_name">linear3D</string>
              <params>
                <real name="linear3D">1</real>
              </params>
            </transform>
          </node>
        </flam3_transform>
        <flam3_shader name="flam3 shader">
          <real name="palette_index">1</real>
          <real name="blend_speed">0.5</real>
          <real name="opacity">1</real>
          <table name="layer_weights">
            <values>1 1 1 1</values>
          </table>
        </flam3_shader>
        <weights_selector name="weights">
          <real name="base_weight">0.5</real>
          <node name="per_iterator_weights">
            <real name="iter 0 weight">1</real>
            <real name="iter 1 weight">1</real>
            <real name="iter 2 weight">1</real>
          </node>
        </weights_selector>
      </iterator>
      <iterator name="iter 1">
        <flam3_transform name="flam3_xform 1">
          <affine2 name="Pre affine">
            <real name="x_axis_angle">17.467311110854343</real>
            <real name="x_axis_length">0.4175383808298346</real>
            <real name="y_axis_angle">107.46731111085435</real>
            <real name="y_axis_length">0.4175383808298346</real>
            <vec2 name="offset">-0.219659 0.299224</vec2>
          </affine2>
          <node name="transforms">
            <transform name="Transform 2">
              <string name="type_name">linear3D</string>
              <params>
                <real name="linear3D">1</real>
              </params>
            </transform>
          </node>
        </flam3_transform>
        <flam3_shader name="flam3 shader">
          <real name="palette_index">0</real>
          <real name="blend_speed">0.5</real>
          <real name="opacity">1</real>
          <table name="layer_weights">
            <values>1 1 1 1</values>
          </table>
        </flam3_shader>
        <weights_selector name="weights">
          <real name="base_weight">0.5</real>
          <node name="per_iterator_weights">
            <real name="iter 0 weight">1</real>
            <real name="iter 1 weight">1</real>
            <real name="iter 2 weight">1</real>
          </node>
        </weights_selector>
      </iterator>
      <iterator name="iter 2">
        <flam3_transform name="flam3_xform 2">
          <affine2 name="Pre affine">
            <real name="x_axis_angle">-19.362429724905475</real>
            <real name="x_axis_length">0.830946093763007</real>
            <real name="y_axis_angle">77.39553838405824</real>
            <real name="y_axis_length">0.7557353951880248</real>
            <vec2 name="offset">-0.191135 -0.009043</vec2>
          </affine2>
          <node name="transforms">
            <transform name="Transform 2">
              <string name="type_name">linear3D</string>
              <params>
                <real name="linear3D">1</real>
              </params>
            </transform>
          </node>
        </flam3_transform>
        <flam3_shader name="flam3 shader">
          <real name="palette_index">1</real>
          <real name="blend_speed">0.5</real>
          <real name="opacity">1</real>
          <table name="layer_weights">
            <values>1 1 1 1</values>
          </table>
        </flam3_shader>
        <weights_selector name="weights">
          <real name="base_weight">0.5</real>
          <node name="per_iterator_weights">
            <real name="iter 0 weight">1</real>
            <real name="iter 1 weight">1</real>
            <real name="iter 2 weight">1</real>
          </node>
        </weights_selector>
      </iterator>
    </node>
  </flam3_IFS>

More Resources
--------------

If you want to know the principles behind making fractals and don't want to wait a year for me to write a bunch of new tutorials, see [my book on making fractals With apophysis](http://www.acm.uiuc.edu/~troys2/ApophysisUserManual/).  That book is written for a different fractal program called Apophysis, but the underlying principles explained in that book are the same for Chaotica.  In fact, this tutorial is adapted from tutorial 1 of that book.  

### The Fractal Community

I'm going to chat for three paragraphs now about two different schools of thought there are in how to make fractals.  The first school of thought are Explorers.  Explorers like to spend hours moving the transforms around, "tweaking" the fractal here and there and trying things to see what happens.  Explorers usually have no idea how to make a particular fractal, just like an explorer often has no idea what will happen as they go into the great unknown.  Explorers don't know the theory or the math behind fractals, and don't care: they just want to poke around and see what happens.  These people are extremely valuable to the community because, over time, they get a sort of 'instinct' for fractals and can tell you how to make specific fractals, and what to do to get a particular effect. They also create entire libraries of fractals and share them.  If the thought of math terrifies you, if you think of yourself as "an artist and not an engineer," then don't worry- you have all the skills you need to be an Explorer.  Explorers make up the vast majority of fractal artists, and have developed many of the more spectacular styles of fractals.  

The second school of thought are the Engineers.  They want to take apart the fractal program and figure out HOW it does what it does, and why exactly putting a Pre-Affine transform in one location makes a tree while putting a Pre-Affine Transform in another location makes a wing.  They'll often study and research for weeks or even months before making a fractal, because they have a very particular fractal in mind that they want to make, and they need to know the math to make it.  Engineers like developing new types of fractals and making the programs the explorers use to make fractals. Engineers are extremely valuable because they often build the software that Explorers use to make incredible fractals.   Without the engineers, Explorers would have no way to explore.  

The two schools of thought combine to form the Chaotica fractal community. In general, the Engineers end up making new varieties of fractals, and give them to the Explorers.  The Explorers take the basic design and tweak it to come up with ever-more-spectacular fractals.  Both produce some spectacular work.  Being an Explorer takes a lot of patience and a willingness to create even when you have absolutely no idea what you are doing.  Being an engineer means being patient, being willing to wade through several thick textbooks, find scarce fractal-making resources, piecing together obscure bits of math and pestering fractal experts on how stuff works until you arrive at a sudden insight.  This is why fractal art is very popular, because the two methods play to the strengths of both artists who hate math and mathematicians who wouldn't know art if it bit them.  One of the things I love best about the fractal art community is that two groups of people who barely talk to each other in real life chat back and forth and use their respective skills to make brilliant art.  

If you want to be a part of this, join the [Chaotica forums](http://chaoticafractals.com/node/17) or [The Aposhack](http://chat.deviantart.com/chat/aposhack) chatroom on Deviantart. (You need a deviantart account to go to the chat room.)  I hang out in both places, as well as dozens of other artists and engineers.  If you have questions, that is the place to ask them.  