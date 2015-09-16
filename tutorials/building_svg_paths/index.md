---
title: 'Building SVG paths'
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](//static.webplatformstaging.org/w/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/SVG/Tutorial/Paths)'
notes:
  - 'Fix broken links'
readiness: 'Almost Ready'
summary: 'This article looks deeply into the SVG &lt;path&gt; element, which is used to create custom shapes.'
tags:
  - Tutorials
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'basic svg shapes'
    - Wikipedia
    - ellipses
    - Canvas
uri: 'tutorials/building svg paths'

---
## Summary

This article looks deeply into the SVG &lt;path&gt; element, which is used to create custom shapes.

As stated in the previous section, the [[\<path\>]] element is the most powerful element in the SVG library of basic shapes. It can be used to create (at least to a fairly good approximation), all the other basic shapes and more.

Additionally, paths can be used to create smooth flowing lines using a relatively few number of control points. Similar looking effects can be created using just the polyline element, but you have to use a lot of points to create a smooth looking effect, and it still won't scale well at larger sizes. So a good understanding of paths is important when drawing SVG. Creating complex paths using an XML editor or text editor still isn't easy, but having an understanding of how they work can make it bearable.

As was said in [the previous section](/w/index.php?title=basic_svg_shapes&action=edit&redlink=1), the shape of a path element is defined by one attribute, `d`. The `d` attribute contains a series of commands and parameters used by those commands. So here we're gonna go through the available commands and see on examples, what they do.

Each of the commands is instantiated by a specific letter. For instance, the "Move to" command is called by the letter M. When the parser runs into this command it knows you want to move to a point. The numbers following it are parameters describing the x and y coordinates you want to move to. So to move to (10,10) you would use the command "M 10 10". After that, the parser begins reading for the next command. All of the commands also come in two variants, one specified with a **capital letter** to specify absolute coordinates on the page, and a second with a **lowercase letter** to specify relative coordinates (e.g. *move from the last point 10px up and 7px to the left*).

Coordinates in the `d` attribute are **always unitless** and hence in the user coordinate system. We will learn later in the tutorial, how paths can be transformed to suit other needs.

## Line commands

There are five line commands for `<path>` nodes. As the name suggests, each one just draws a straight line between two points. The first is the "Move To" command, M, which was described above. Again, it takes in two parameters, an x coordinate and y coordinate to move to. If your cursor already was somewhere on the page, no line is drawn to connect the two places. The "Move To" command appears at the beginning of paths to specify where the drawing should start.

    M x y

or

    m dx dy

It's good to draw examples as we go here. Unfortunately, we haven't drawn anything yet. All we've done is move the start point for our path, so we won't see anything yet. I am going to show each of the points we draw as we go to 'em, so in the following example we just have a point at (10,10). Note though, that it wouldn't show up if you were just drawing the path.

![Blank Path Area.png](//static.webplatformstaging.org/w/public/5/58/Blank_Path_Area.png)

    <?xml version="1.0" standalone="no"?>

    <svg width="200px" height="200px" version="1.1" xmlns="http://www.w3.org/2000/svg">

      <path d="M10 10"/>

      <!-- Points -->
      <circle cx="10" cy="10" r="2" fill="red"/>

    </svg>

There are three commands that draw actual lines. The most generic is the "Line To" command, `L`. `L` takes two parameters, and x and a y coordinate, and draws a line from your current position to the second one.

     L x y (or l dx dy)

There are two abbreviated forms for this when you're just drawing a horizontal or vertical line. `H`, draws a horizontal line, and `V` draws a vertical one. Both of them only take one argument since they only move in one direction.

    H x (or h dx)
     V y (or v dy)

So now we know enough commands to start to draw something. An easy place to start is just drawing a plain old rectangle (the same type that could more easily be made with a `<rect>` element). Its composed of only horizontal and vertical lines, so its a pretty good example of all three of the previous "Line To" bits:

![Path Line Commands.png](//static.webplatformstaging.org/w/public/b/ba/Path_Line_Commands.png)

    <?xml version="1.0" standalone="no"?>

    <svg width="100px" height="100px" version="1.1" xmlns="http://www.w3.org/2000/svg">

      <path d="M10 10 H 90 V 90 H 10 L 10 10"/>

      <!-- Points -->
      <circle cx="10" cy="10" r="2" fill="red"/>
      <circle cx="90" cy="90" r="2" fill="red"/>
      <circle cx="90" cy="10" r="2" fill="red"/>
      <circle cx="10" cy="90" r="2" fill="red"/>

    </svg>

Finally, we can shorten the above path a little bit by using the "Close Path" command, `Z`. This command draws a straight line from your current position back to the first point that started the path. Its often placed at the end of a path node, although its not necessary to close a path all the time. Apparently there is no difference between the uppercase and lowercase command.

    Z (or z)

So our path above could be shortened to:

    <path d="M10 10 H 90 V 90 H 10 Z" fill="transparent" stroke="black"/>

You can also use the relative form of these commands to draw the same picture. As was mentioned earlier, relative commands are called by using lowercase letters, and rather than moving the cursor to an exact coordinate, they move it relative to its last position. For instance, since our box is 80 x 80, the path element could have been written:

    <path d="M10 10 h 80 v 80 h -80 Z" fill="transparent" stroke="black"/>

The path will move to point (10,10) and the move horizontally 80 points to the left, then 80 points down, then 80 points to the left, and then back to the start.

You may be wondering what use these commands have when the `<polygon>` or `<polyline>` element can do the same thing. The answer is that they don't do much more. If you're only drawing straight lines, it is probably better grammatically to use one of the other forms. However, paths are used so much in drawing SVG that developers get used to them, and you'll see them instead. As far as I know, there's no real performance penalty or bonus for using one or the other. Generating paths through script might be another matter, as the path command syntax is slightly more complicated than the other two, which just take points.

## Curve commands

There are 3 different commands that can be used to create smooth curves. Two of those curves are Bezier curves, and the third one is an "arc" or part of a circle. You might have already gained practical experience with Bezier curves, if you used path tools in Inkscape, Illustrator or Photoshop. For a complete description of the math behind Bezier curves you'll have to go to a reference like the one on [Wikipedia](/w/index.php?title=Wikipedia&action=edit&redlink=1). It's too much information to try and cover here. There are an infinite number of different types of Bezier curves, but only two simple ones are available in path elements: a cubic one, C, and a quadratic one, Q.

### Bezier Curves

So we'll start with the slightly more complex Bezier curve, the cubic one, C. Cubic Beziers take in two control points for each point. As such, you have to specify three sets of coordinates when you want to create a cubic Bezier

     C x1 y1, x2 y2, x y (or c dx1 dy1, dx2 dy2, dx dy)

The last set of coordinates here (x,y) are where you want the line to end. The other two are control points. (x1,y1) is the control point for the start of your curve, and (x2,y2) for the end point of your curve. If you are familiar with algebra or calculus, the control points essentially describe the slope of your line starting at each point. The Bezier function then creates a smooth curve that transfers you from the slope you established at the beginning of your line, to the slope at the other end.

![Cubic Bezier Curves.png](//static.webplatformstaging.org/w/public/2/2c/Cubic_Bezier_Curves.png)

    <?xml version="1.0" standalone="no"?>

    <svg width="190px" height="160px" version="1.1" xmlns="http://www.w3.org/2000/svg">

      <path d="M10 10 C 20 20, 40 20, 50 10" stroke="black" fill="transparent"/>
      <path d="M70 10 C 70 20, 120 20, 120 10" stroke="black" fill="transparent"/>
      <path d="M130 10 C 120 20, 180 20, 170 10" stroke="black" fill="transparent"/>
      <path d="M10 60 C 20 80, 40 80, 50 60" stroke="black" fill="transparent"/>
      <path d="M70 60 C 70 80, 110 80, 110 60" stroke="black" fill="transparent"/>
      <path d="M130 60 C 120 80, 180 80, 170 60" stroke="black" fill="transparent"/>
      <path d="M10 110 C 20 140, 40 140, 50 110" stroke="black" fill="transparent"/>
      <path d="M70 110 C 70 140, 110 140, 110 110" stroke="black" fill="transparent"/>
      <path d="M130 110 C 120 140, 180 140, 170 110" stroke="black" fill="transparent"/>

    </svg>

The example above creates nine Cubic Bezier curves. I regret that at this point, drawing all the control points in the above code would make it fairly large so they've been left out. You can draw them on your own if you want to draw the exact figure shown yourself. As the curves move toward the left the control points become more spread out horizontally. As it moves towards the right, they become further separated from the end points. The thing to note here is that the curve starts out in the direction of the first control point, and then bends so that it arrives along the direction of the second control point.

You can string several Bezier curves to create long smooth shapes. Often in this case, the control point on one side of a point will be a reflection of the control point used on the other side (to keep the slope constant). In this case, you can use a shortcut version of the cubic Bezier, designated by the command `S` (or `s`).

    S x2 y2, x y (or s dx2 dy2, dx dy)

`S` produces the same type of curve as earlier, but if it follows another `S` command or a `C` command, the first control point is assumed to be a reflection of the one used previously. If the `S` command doesn't follow another `S` or `C` command, then it is assumed that both control points for the curve are the same. An example of this syntax is shown below, and in the figure to the left the specified control points are shown in red, and the inferred control point in blue.

![ShortCut Cubic Bezier.png](//static.webplatformstaging.org/w/public/4/43/ShortCut_Cubic_Bezier.png)

    <?xml version="1.0" standalone="no"?>
    <svg width="190px" height="160px" version="1.1" xmlns="http://www.w3.org/2000/svg">
      <path d="M10 80 C 40 10, 65 10, 95 80 S 150 150, 180 80" stroke="black" fill="transparent"/>
    </svg>

The other type of Bezier curve that is available is a quadratic Bezier, Q. Its actually a simpler curve than the cubic one. Basically it only requires one control point, which determines the slope of the curve at both the start point, and at the end point, as such it takes two arguments, the control point and the end point of the curve

    Q x1 y1, x y (or q dx1 dy1, dx dy)

![Quadratic Bezier.png](//static.webplatformstaging.org/w/public/5/59/Quadratic_Bezier.png)

    <?xml version="1.0" standalone="no"?>
    <svg width="190px" height="160px" version="1.1" xmlns="http://www.w3.org/2000/svg"">
      <path d="M10 80 Q 95 10 180 80" stroke="black" fill="transparent"/>
    </svg>

As with the cubic Bezier curve, there is a shortcut for stringing together long sets of them quadratic Beziers, T.

    T x y (or t dx dy)

As before, the shortcut looks at the previous control point you used, and infers a new one from it. This means that after your first control point, you can make fairly complex shapes by specifying only end points. Note that this only works if the previous command was a Q or a T command. If it is not, then the control point is assumed to be the same as the previous point, and you'll only draw lines.

![Shortcut Quadratic Bezier.png](//static.webplatformstaging.org/w/public/f/f2/Shortcut_Quadratic_Bezier.png)

    <?xml version="1.0" standalone="no"?>
    <svg width="190px" height="160px" version="1.1" xmlns="http://www.w3.org/2000/svg">
      <path d="M10 80 Q 52.5 10, 95 80 T 180 80" stroke="black" fill="transparent"/>
    </svg>

Both curves produce fairly similar results, although the cubic allows you greater freedom in exactly what your curve looks like. Deciding which to use often just depends on the situations and amount of symmetry your line has.

### Arcs

The other type of curved line you can create using SVG is the arc, A. Arcs are essentially sections of circles or ellipses. For a given x-radius and y-radius, there are two ellipses that can connect any two points (as long as they're within the radius of the circle). Along either of those circles there are two possible paths that you can take to connect the points, so in any situation there are four possible arcs available. Because of that, arcs have to take in quite a few arguments:

    A rx ry x-axis-rotation large-arc-flag sweep-flag x y
     a rx ry x-axis-rotation large-arc-flag sweep-flag dx dy

At its start the arc element takes in two arguments for the x-radius and y-radius of the arc. Those seem pretty self explanatory, but if you need to, look up [ellipses](/w/index.php?title=ellipses&action=edit&redlink=1) to see how they behave. The third parameter describes the rotation of the arc. This is best explained with an example:

![SVGArcs XAxisRotation.png](//static.webplatformstaging.org/w/public/a/a5/SVGArcs_XAxisRotation.png)

    <?xml version="1.0" standalone="no"?>
    <svg width="320px" height="320px" version="1.1" xmlns="http://www.w3.org/2000/svg">
      <path d="M10 315
               L 110 215
               A 30 50 0 0 1 162.55 162.45
               L 172.55 152.45
               A 30 50 -45 0 1 215.1 109.9
               L 315 10" stroke="black" fill="green" stroke-width="2" fill-opacity="0.5"/>
    </svg>

The example shows a path element that goes diagonally across the page. In the middle of it, two elliptical arcs have been cut out (x radius = 30, y radius = 50). In the first one, the x-axis-rotation has been left at 0, so the ellipse that the arc travels around (shown in gray), is oriented straight up and down. For the second arc though, the x-axis-rotation is set to -45 degrees. This rotates the ellipse so that it is aligned with its minor axis along the path direction, as shown by the second ellipse in the example image.

The four different paths mentioned above are determined by next two flags in the argument. As mentioned earlier, there are still two possible ellipses for the path to travel around, and two different possible paths on both those ellipses giving four possible paths. The first argument here is the large-arc-sweep-flag. It simply determines if the arc that should be drawn should be greater than, or less than 180 degrees, and in the end determines which direction the arc will travel around a given circle. The second argument determines if the arc should begin moving at negative angles or positive ones, which essentially picks which of the two circles you will travel around. The example below shows all four possible combinations, along with the two circles for each case.

![SVGArcs Flags.png](//static.webplatformstaging.org/w/public/8/83/SVGArcs_Flags.png)

    <?xml version="1.0" standalone="no"?>
    <svg width="325px" height="325px" version="1.1" xmlns="http://www.w3.org/2000/svg">
      <path d="M80 80
               A 45 45, 0, 0, 0, 125 125
               L 125 80 Z" fill="green"/>
      <path d="M230 80
               A 45 45, 0, 1, 0, 275 125
               L 275 80 Z" fill="red"/>
      <path d="M80 230
               A 45 45, 0, 0, 1, 125 275
               L 125 230 Z" fill="purple"/>
      <path d="M230 230
               A 45 45, 0, 1, 1, 275 275
               L 275 230 Z" fill="blue"/>
    </svg>

The final two arguments, if you haven't guessed yet, designate the x and y coordinates to end the stroke at. Arcs are an easy way to create pieces of circles or ellipses in your drawings. For instance, a *pie chart* would require you create a different arc for each piece.

If you're transitioning to SVG from [Canvas](/w/index.php?title=Canvas&action=edit&redlink=1), arcs can be the hardest thing to move, but are also much more powerful. Complete circles and ellipses are actually the one object paths have trouble drawing. Because the start and end points for any path going around a circle are the same, there are an infinite number of circles that could be chosen, and the actual path is undefined. It's possible to approximate them by making the start and end points of your path slightly askew, and then connecting them with another path segment. At that point, it's often easier to use a real circle or ellipses node instead.
