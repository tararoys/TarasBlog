Title: Intro To Fractals: Making An Angel's Wing
Author: Tara Roys
Date: Wed Sept 12 2013 10:16:51 GMT-0600 (CST)
Node: v0.1.102

Making Angel Wings: An Introduction to Apohysis
===============================================

Introduction
============

<img srcwing/images/wingtutorialcolored3.jpg)

This tutorial assumes you have zero knowledge of fractals or of
Apophysis.

In order to use Apophysis, you must use Windows. (There are a few
versions( specifically Apophysis-J) that can be used on all operating
systems, but I have no experience with these.) The latest versions of
Apophysis can be downloaded for free from [the Apophysis
website.](http://www.apophysis.org) Apophysis is also extensively
modified by several independent hackers. Links to their versions can be
found in several places, but are usually posted to the Deviant Art
fractal community at [Deviant Art Fractal
Community.](http://apophysis.deviantart.com)

This chapter will teach you how to make the fractal wing shown above. By
the end of it, you will know how to use the most important parts of the
Apophysis user interface, and you'll have a pretty picture to boot.

The Main Screen
===============

This tutorial is a general introduction to Apophysis. It introduces all
of the important aspects of the program by teaching how to make an
angels wing. So, without further ado, let me present "How to Make An
Angel's Wing" by yours truly, [Tara
Roys.](http://tararoys.deviantart.com)

![](wing/images/apophysismain.jpg)

First, open up Apophysis. You will see three things of interest: the
main screen, as shown above, which will hopefully be displaying a pretty
fractal, the left-hand list of fractals,and a series of menus and
buttons across the top. The main window displays a fractal. Ignore it
for the moment. The left-hand list is a list of 100 randomly generated
fractals. You can click on them and look in the main window to see if
you see anything interesting. After that, turn your attention to the
menus.

Moving Your Fractal: The Transform Editor
=========================================

![](wing/images/menus.jpg)

Click on the Transform Editor button. ![](wing/images/editorbutton.jpg)A
new window called the Transform Editor will open, as shown below.

![](wing/images/transformeditor.jpg)

Moving around in the Transform Editor
-------------------------------------

When you open the transform editor, the first thing you'll see is
probably a large black screen with some triangles and a grid on it..

The first thing you'll wand to learn is how to move around in this
window.

Right-click and hold on the black grid. Your mouse will turn into a
Translation symbol ![](wing/images/transformiconnomouse.png) . Still
holding the right mouse button down, move your mouse around. You'll drag
the grid around. This lets you reposition your editor window so that you
can concentrate on whatever part you want.

To zoom in and out of your editor window, scroll with the mouse wheel.
Scrolling up will zoom in, whereas scrolling down will zoom out. If you
don't have a mouse wheel, you can zoom by using the + and - keys across
the top of your keyboard (not the ones on the number pad, but the ones
that also double as underscore and equals.

Making a New Blank Flame
------------------------

In the upper left-hand corner of the transform editor, you will see the
new blank flame button. ![](wing/images/newblankflame.jpg) Click on it.

![](wing/images/transformeditorblankflame.jpg)

You will see a single red triangle in your transform editor.

The first thing you should note is the large black grid with the
triangle. This triangle is called a transform, because changing it
transforms the fractal into strange and different shapes. I shall call
it a transform from now on.

Note: The words "transform" and "triangle" have different meanings in
Apophysis. If you look on the right side of the transform editor, you'll
notice that there is a tab that says 'triangle' and a tab that says
'transform.' Both tabs have stuff in them that you can press with your
mouse or type in numbers that will move the triangle around. Both do it
in slightly different ways that, unless you know the reasons behind
them, will drive you crazy. Heck, I know the reasons behind them, and
they still drive me crazy. But I'm getting ahead of myself: the reasons
will be explained in the next chapter.

Moving Transforms With the Mouse
--------------------------------

### Moving the Whole Transform

Hover your mouse over the red triangle until the move icon shows up.
Click and hold down the left mouse button to drag the triangle. When you
click, two white axis lines will appear, as seen below. Drag the
transform. You will notice that two dull gray axis lines will follow the
triangle, another pair of dull gray axis lines stay behind, as seen
below. The lines that stay behind show where you were moving from, while
the lines that follow the triangle tell where you are moving to.

### The Reference Transform

Let go of the transform. The next thing to notice is the gray triangle
we just uncovered. That gray triangle is called the reference transform.
You'll learn more about why the reference transform is important in
later tutorials. For right now, you'll use it to help measure where to
put your other transforms.

![](wing/images/transformeditorreferencetransform.jpg)

You can't move the gray reference transform. However, you can move the
red triangle.

### Scaling the Transform

Let's learn a couple more ways to move the red triangle with the mouse.
Notice that the red triangle has two solid red lines and a dotted red
line. Hover your mouse over the dotted red line until the scale
icon![](wing/images/mousescale.png) appears beside the mouse pointer.
The dotted line will also be highlighted. This means that you can make
the transform bigger or smaller. Click and hold on it with the left
mouse button and drag to make the transform bigger or smaller.

![](wing/images/transformeditorscale.jpg)

### Rotating the Transform

Now hover your mouse over one of the solid red lines on the transform
until the rotate icon ![](wing/images/mousewithrotate.png) appears. The
line you are hovering over will also highlight. Click and hold with the
left mouse button. A circle and two white axis lines will appear. The
circle is centered around where the transform will rotate, as shown
below.

![](wing/images/transformeditorrotate.jpg)

Drag the mouse to rotate the transform.

![](wing/images/transformeditorrotate2.jpg)

### Moving the Transform with the O point

The next thing to notice is that each point on the triangle is labeled.
One is labeled O, one is labeled X, and one is labeled Y.

Hover your mouse over the O point until the translate icon
![](wing/images/mousewithtranslate.png) shows up. The 0 point will
highlight white. ![](wing/images/Ohighlightwhite.jpg) Left-click and
hold on the O point. You will notice two pairs of axis lines appear, as
seen below.

These axis lines are slightly different than the lines you saw earlier
when selecting the whole transform and moving it. First, one pair always
stays on the X and Y axis, instead of staying behind where the transform
used to be. The other pair follows the transform around as usual.

So why is there a difference between moving with the O point and moving
the whole triangle? O is shorthand for origin. If you notice, the
reference transform has an O point as well, and one pair of axis lines
always goes through it. The reference transform's O point is the origin
of the grid you are drawing your fractal on, and the red transform's O
point shows how far from that origin your transform has moved, because
that distance is important in the making of the fractal. When you use
the O point to move the transform, Apophysis assumes that you want to
know the distance between the reference transform's O point the red
transform's O point, and puts the axis lines in to help show you that
distance, as seen below.

![](wing/images/transformeditorOwithaxisdistance.jpg)

By contrast, when you move the whole transform, Apophysis assumes you
want to know where the red transform was before you started moving it,
and so leaves a pair of axis lines to show where the red transform's O
point used to be before you started moving it, as seen below.

![](wing/images/transformeditorwithaxisdistance.jpg)

### Skewing the Transform With the X and Y Points

Now let's take a look at the other two points on the triangle: the X
point and the Y point.

Let's start with the X point.

Hover your mouse over the X point until the translate icon
![](wing/images/mousewithtranslate.png) shows up. The X point will
highlight red. ![](wing/images/Xhighlightred.jpg) Left click and hold on
the X point and start dragging it around. You'll notice ttwo pairs of
axis lines appear, and you'll also notice that only the x point
moves--the whole transform does not move. This allows you to skew the
transform.

![](wing/images/Xmove.jpg)

Notice that one pair of axis lines goes through the O point on the
transform, and other pair of axis lines goes through the X. This is
because Apophysis thinks it is important for you to know the distance
between the O point and the X point, because that distance is important
when forming the fractal. Because of this Apophysis places the axis
lines so that you can see the distance.

Moving the Y point acts exactly the same as moving the X point, with the
sole exception that when you hover your mouse over the Y point it turns
blue. ![](wing/images/Yhighlightblue.jpg)

Now that we know how to move one transform, let's give ourselves a few
more transforms to play with.

### The Transform Selection Dropdown Menu

Click on the red transform to select it.

On the right-hand side of the Transform Editor, you will see the
Selected Transform Menu. ![](wing/images/transformmenu.jpg) If you click
on the arrow, ![](wing/images/dropdownarrow.jpg) a drop-down menu will
appear. ![](wing/images/transformdropdown.jpg)

Right now the dropdown menu only has one transform, but as you add more
transforms to your fractal the Selected Transform Menu will help you
manage them.

### Adding More Transforms

Up until now, our fractal has been a bit boring. In order to have a wing
by the end of this, we need to add a few more transforms. Specifically,
two more transforms. Go to the top of the Transform Editor and click on
the add transform ![](wing/images/addtransformbutton.jpg) button. This
will add a new transform on top of the reference triangle. You'll notice
that it's yellow, and also notice that the Selected Transform Menu now
shows another transform, as seen below.

![](wing/images/transformeditortwotransforms.jpg)

Click the new transform button ![](wing/images/addtransformbutton.jpg)
again. This will add another new transform, this time in green. You'll
notice that you can no longer see the yellow transform because it is
hidden by the green triangle.

![](wing/images/transformeditor3triangles.jpg)

This can sometimes cause problems you want to move the yellow transform
with the mouse, because at first glance it seems like you have to move
the green transform first. If you use just a mouse, you will have to
move the green transform first. This does not really matter for this
tutorial, but when working with later fractals there will be times when
you want to move transforms that are hidden below other transforms. In
that case, you will need to move the transforms using either the
Transform tab or the Triangle tab.

Up until now, our fractal has been a bit boring- just a blank screen, or
perhaps a blur. But now we get to the fun part, where we start seeing
things!

### Put It All Together

All right. You know how to move transforms. Now lets use them to make a
pretty fractal.

Move your transforms into this arrangement:

![](wing/images/finalwingarrangement.jpg)

The closer you get to this exact arrangement, the more your fractal will
look like a wing. You can see the image it is supposed to look like in
the preview window in the upper right-hand corner of the fractal box.

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

The parameters for the wing in various stages of construction can be
found [here](wing/wingtutorial.flame)
