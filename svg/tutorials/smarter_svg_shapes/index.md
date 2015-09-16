---
title: SVG basic shapes and text
notes:
  - 'Fix multiple broken links'
readiness: 'In Progress'
summary: 'This guide introduces SVG''s basic graphic elements, from simple lines and shapes to complex polygons and freehand paths. It also shows how to place lines of text and wrap it around curved paths.'
tags:
  - Tutorials
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - svg/attributes/width
    - svg/attributes/height
    - svg/attributes/x
    - svg/attributes/y
    - svg/attributes/cx
    - svg/attributes/cy
    - svg/attributes/r
    - svg/attributes/rx
    - svg/attributes/ry
    - svg/properties/fill
    - svg/properties/stroke
    - svg/properties/stroke-width
    - svg/properties/fill-opacity
    - svg/properties/stroke-opacity
    - svg/attributes/points
    - svg/properties/stroke-linecap
    - svg/properties/stroke-linejoin
    - svg/properties/stroke-miterlimit
    - svg/properties/stroke-dasharray
    - svg/properties/stroke-dashoffset
    - svg/attributes/d
    - svg/properties/fill-rule
    - svg/properties/marker-start
    - svg/properties/marker-mid
    - svg/properties/marker
    - svg/attributes/orient
    - css/properties/text-anchor
    - svg/attributes/dy
    - svg/attributes/rotate
    - svg/attributes/dx
    - svg/elements/tref
    - svg/attributes/startOffset
uri: 'svg/tutorials/smarter svg shapes'

---
**By Mike Sierra**

## Summary

This guide introduces SVG's basic graphic elements, from simple lines and shapes to complex polygons and freehand paths. It also shows how to place lines of text and wrap it around curved paths.

## Simple shapes

Various SVG elements produce basic shapes, and their attributes specify their dimensions.

Rectangles are defined by their [**width**](/w/index.php?title=svg/attributes/width&action=edit&redlink=1) and [**height**](/w/index.php?title=svg/attributes/height&action=edit&redlink=1) attributes, while [**x**](/w/index.php?title=svg/attributes/x&action=edit&redlink=1) and [**y**](/w/index.php?title=svg/attributes/y&action=edit&redlink=1) offsets position the upper-left corner of the [**rect**](/svg/elements/rect) relative to its parent:

``` xml
<rect x="10" y="10" width="240" height="160"/>
```

 Circles are positioned by the [**cx**](/w/index.php?title=svg/attributes/cx&action=edit&redlink=1) and [**cy**](/w/index.php?title=svg/attributes/cy&action=edit&redlink=1) center point, and the radius ([**r**](/w/index.php?title=svg/attributes/r&action=edit&redlink=1)) specifies the size:

``` xml
<circle cx="50" cy="50" r="100"/>
```

 Ellipses are positioned like circles, but require two [**rx**](/w/index.php?title=svg/attributes/rx&action=edit&redlink=1) and [**ry**](/w/index.php?title=svg/attributes/ry&action=edit&redlink=1) radius attributes for each axis:

``` xml
<ellipse cx="40" cy="60" rx="40" ry="20"/>
```

 When applied to [**rect**](/svg/elements/rect) elements, [**rx**](/w/index.php?title=svg/attributes/rx&action=edit&redlink=1) and [**ry**](/w/index.php?title=svg/attributes/ry&action=edit&redlink=1) attributes produce rounded corners:

``` xml
<rect x="10" y="10" width="160" height="240" rx="20" ry="20"/>
```

 This is how these examples appear:

![svg shapes.png](/assets/public/7/74/svg_shapes.png)

## Fill and stroke properties

By default, shapes are filled black. The [**fill**](/w/index.php?title=svg/properties/fill&action=edit&redlink=1) and [**stroke**](/w/index.php?title=svg/properties/stroke&action=edit&redlink=1) properties specify the color of the background and the edge of the shape.

``` xml
<rect fill="pink" stroke="red" x="10" y="10" width="160" height="240"/>
```

 You can assign these as attributes on SVG elements, but they are really CSS properties. For the sake of clarity and best practice, this guide expresses SVG properties as CSS selectors:

``` css
 rect {
     fill   : pink;
     stroke : red;
 }
```

 Properties specified via CSS override those specified as attributes, so this local CSS that colors the [**rect**](/svg/elements/rect) green overrides the local attribute that colors it red:

``` xml
<rect fill="pink" stroke="red" style="fill:lightgreen;stroke:green"
    x="10" y="10" width="160" height="240"/>
```

 The [**stroke-width**](/w/index.php?title=svg/properties/stroke-width&action=edit&redlink=1) is centered over the edge of the shape, so increasing its pixel value bleeds the [**stroke**](/w/index.php?title=svg/properties/stroke&action=edit&redlink=1) color both inside and outside the shape:

``` css
 rect {
     fill         : pink;
     stroke       : red;
     stroke-width : 6;
 }
```

 To apply transparencies, you can set the [**fill-opacity**](/w/index.php?title=svg/properties/fill-opacity&action=edit&redlink=1) and [**stroke-opacity**](/w/index.php?title=svg/properties/stroke-opacity&action=edit&redlink=1) properties.

``` css
 rect {
     stroke-width   : 10;
     stroke         : red;
     stroke-opacity : 0.5;
     fill           : red;
     fill-opacity   : 0.25;
 }
```

 ![svg opacity.png](/assets/public/4/44/svg_opacity.png)

Alternately, you can use [**rgba()** and **hsla()**](/css/data_types/color) CSS colors to to incorpoarate opacity as part of [**fill**](/w/index.php?title=svg/properties/fill&action=edit&redlink=1) and [**stroke**](/w/index.php?title=svg/properties/stroke&action=edit&redlink=1) property values. The following has the same effect as the example above:

``` css
 rect {
     stroke-width : 10;
     stroke       : rgba(100%,0%,0%,0.5);
     fill         : rgba(100%,0%,0%,0.25);
 }
```

## Lines and polygons

To draw a straight line, specify its start and end coordinates as **x1**, **y1**, **x2**, and **y2**:

``` xml
<line x1="0" y1="0" x2="100" y2="100"/>
```

 A [**polyline**](/svg/elements/polyline) consists of a series of *x*/*y* coordinates specified within the [**points**](/w/index.php?title=svg/attributes/points&action=edit&redlink=1) attribute, with items separated by either commas or whitespace. This draws an arrow:

``` xml
<polyline points="100,225 100,115 130,115 70,15 70,15 10,115 40,115 40,225"/>
```

 A [**polygon**](/svg/elements/polygon) is the same as a [**polyline**](/svg/elements/polyline), but the final coordinate is joined with the first:

``` xml
<polygon points="100,225 100,115 130,115 70,15 70,15 10,115 40,115 40,225"/>
```

 ![svg linepath.png](/assets/public/a/a4/svg_linepath.png)

## More stroke properties

Additional properties provide greater control over how the ends or joints of line segments appear. The [**stroke-linecap**](/w/index.php?title=svg/properties/stroke-linecap&action=edit&redlink=1) property determines the appearance of the end of a stroke, or dashes within a stroke. Options appear as follows, with both **round** and **square** extending past the end of the line depending on the [**stroke-width**](/w/index.php?title=svg/properties/stroke-width&action=edit&redlink=1)::

![svg linecap round.png](/assets/public/c/c1/svg_linecap_round.png)

    stroke-linecap: round;

![svg linecap square.png](/assets/public/c/c1/svg_linecap_square.png)

    stroke-linecap: square;

![svg linecap butt.png](/assets/public/d/da/svg_linecap_butt.png)

    stroke-linecap: butt;

The [**stroke-linejoin**](/w/index.php?title=svg/properties/stroke-linejoin&action=edit&redlink=1) property affects how joined segments appear, and becomes more apparent for narrower angles as the [**stroke-width**](/w/index.php?title=svg/properties/stroke-width&action=edit&redlink=1) increases:

![svg linejoin round.png](/assets/public/d/d7/svg_linejoin_round.png)

    stroke-linejoin: round;

![svg linejoin bevel.png](/assets/public/1/16/svg_linejoin_bevel.png)

    stroke-linejoin: bevel;

![svg linejoin miter.png](/assets/public/b/b1/svg_linejoin_miter.png)

    stroke-linejoin: miter;

Setting [**stroke-linejoin**](/w/index.php?title=svg/properties/stroke-linejoin&action=edit&redlink=1) to **bevel** diagonally shaves the points from angles, and setting it to **miter** allows them to protrude. The [**stroke-miterlimit**](/w/index.php?title=svg/properties/stroke-miterlimit&action=edit&redlink=1) property limits how much of the angle is allowed to protrude, expressed relative to the [**stroke-width**](/w/index.php?title=svg/properties/stroke-width&action=edit&redlink=1). This example only bevels those angles that protrude twice the width:

![svg linejoin miterlimit.png](/assets/public/4/42/svg_linejoin_miterlimit.png)

    polygon {
      stroke-linejoin   : miter;
      stroke-miterlimit : 2;
      stroke-width      : 10;
    }

The [**stroke-dasharray**](/w/index.php?title=svg/properties/stroke-dasharray&action=edit&redlink=1) property allows you define arbitrary dash patterns as a comma-separated list of pixel values. A value of *20,10,10,10* draws a dash 20 pixels long, followed by a gap of 10 pixels before the following 10-pixel dash, another gap, followed the same pattern repeated to the end of the shape:

![svg stroke dasharray.png](/assets/public/1/17/svg_stroke_dasharray.png)

    stroke-dasharray: 20,10,10,10;

The [**stroke-dashoffset**](/w/index.php?title=svg/properties/stroke-dashoffset&action=edit&redlink=1) property allows you to shift the number of pixels at which the dash pattern begins.

## Simple paths

Paths are complex shapes that may feature discontinuous series of lines and curves. The [**path**](/svg/elements/path) element's [**d**](/w/index.php?title=svg/attributes/d&action=edit&redlink=1) (definition) attribute specifies a sequence of commands referencing pairs of *x*/*y* coordinates within the drawing area.

The following [interactive path-building utility](http://letmespellitoutforyou.com/samples/svg_path.html) allows you to create your own path definitions using all the commands detailed below, and see them reflected in SVG code. Choose the command you want, then click within the drawing area to provide each command with a set of coordinates:

![svg path.png](/assets/thumb/d/dc/svg_path.png/600px-svg_path.png)

The simplest path commands drop a pen at one coordinate and draw a line to another. In this example, the **M** (move) command places the drawing point at the *100,225* coordinate. The **L** (line) command draws a line to *100,115*, and subsequent **L** commands draw the same arrow-shaped polygon shown above, starting from its bottom-left corner and drawing in a clockwise direction:

``` xml
<path d="M 100,225 L 100,115 L 130,115 L 70,15 L 10,115 L 40,115 L 40,225 z"/>
```

 ![svg linepath.png](/assets/public/a/a4/svg_linepath.png)

The **z** command at the end draws a final line to the most recent **M** coordinate to close off the box. At any point along the path, you may use **M** to place the drawing point elsewhere to create discontinuous segments known as *subpaths*, which may appear to be separate objects.

Coordinates and commands can be separated by any combination of commas or whitespace characters. (To clarify these examples, commas separate each *x,y* pair.)

The uppercase **M** and **L** commands above specify absolute coordinates. For all uppercase commands described here, there are alternative lowercase commands that specify coordinates in terms relative to the previously defined coordinate. Starting from the default *0,0* origin point, the following path defines the same shape as the one above using **m** and **l** commands:

``` xml
<path d="m 100,225 l 0,-110 l 30,0 l -60,-100 l -60,100 l 30,0 l 0,110 z" />
```

 The **H** and **V** commands, and their **h** and **v** alternatives, draw a horizontal or vertical line to the specified coordinate.

## Curved paths

Unlike polygons, paths can incorporate curves. Bézier curves require additional *control point* coordinates that do not render but that influence the shape of the curve.

The **Q** and **q** commands define a *quadratic* Bézier curve using one control point coordinate followed by another coordinate where the curve segment ends. The **C** and **c** commands use two intervening control points to define a more complex *cubic* Bézier curve. These examples show where each control point falls:

![svg quadratic.png](/assets/public/8/89/svg_quadratic.png)

``` xml
  <!-- quadratic -->
<path d="M 50,100 Q 180,20 300,130"/>
```

![svg cubic.png](/assets/public/1/1d/svg_cubic.png)

``` xml
  <!-- cubic -->
<path d="M 50,120 C 130,50 250,150 280,100"/>
```

Adding additional sets of controls points has the same effect as adding additional **Q**/**q**/**C**/**c** commands. The following definition pairs produce the same sequence of quadratic and cubic curves, but the second line leaves out the redundant command:

![svg quadratic poly.png](/assets/public/f/f6/svg_quadratic_poly.png)

``` xml
  <!-- quadratic, chained -->
<path d="M 50,100 Q 180,20 300,130 Q 320,20 400,50"/>
<path d="M 50,100 Q 180,20 300,130   320,20 400,50"/>
```

 ![svg cubic poly.png](/assets/public/f/f8/svg_cubic_poly.png)

``` xml
  <!-- cubic, chained -->
<path d="M 50,120 C 130,50 250,150 280,100 C 250,50 450,50 400,100"/>
<path d="M 50,120 C 130,50 250,150 280,100   250,50 450,50 400,100"/>
```

 In both of these examples, the curve segments join abruptly at an angle. The **T** and **t** commands are designed to produce quadratic curves that transition smoothly from the previous curve. They work by extrapolating a control point from the previous control point on the other side of the previous destination point, effectively mirroring it to produce waves. The following two path definitions produce the same sequence of curves. The first uses the **T** command to extrapolate the extra control point (marked red), while the second uses a second **Q** command to explicitly define it. Both specify the same destination point:

``` xml
<path d="M 50,100 Q 180,20 300,130 T         400,50"/>
<path d="M 50,100 Q 180,20 300,130 Q 420,240 400,50"/>
```

 ![svg quadratic smooth.png](/assets/public/1/1f/svg_quadratic_smooth.png)

The **S** and **s** commands perform the same kind of mirroring to produce smooth cubic Bézier curves suitable for freehand drawing. Since Bézier curves are defined by two control points, the first supplied coordinate specifies the second control point, and the second coordinate specifies the end point. The following two path definitions produce the same sequence of curves, the second substituting the **C** command to explicitly define the extra control point, again marked red:

``` xml
<path d="M 50,120 C 130,50 250,150 280,100 S        450,50 400,100"/>
<path d="M 50,120 C 130,50 250,150 280,100 C 310,50 450,50 400,100"/>
```

 ![svg cubic smooth.png](/assets/public/d/d0/svg_cubic_smooth.png)

The **A** and **a** commands specify an *elliptical arc*, using syntax specifying a surprisingly great deal of information:

-   A pair of radius measurements defining the ellipse's size and shape, equivalent to the [**ellipse**](/svg/elements/ellipse) element's [**rx**](/w/index.php?title=svg/attributes/rx&action=edit&redlink=1) and [**ry**](/w/index.php?title=svg/attributes/ry&action=edit&redlink=1) attributes.

-   A measurement indicating the degree to which the ellipse is rotated.

-   A *large-arc* flag (*0* or *1*) indicating whether to travel to the destination point via the longer arc that exceeds 180°.

-   To distinguish between the two possible arcs that mirror each other along the line to the destination point, a *sweep-arc* flag (*0* or *1*) specifies whether to prefer whichever renders in a clockwise direction.

-   A final set of coordinates indicates the ellipse's end point.

If the ellipse's radii is insufficient or if its rotation makes it impossible to get to the final end point, the ellipse does not render.

Elliptical arcs are great for drawing parts of clouds and thought balloons:

![svg arc.png](/assets/thumb/8/8b/svg_arc.png/300px-svg_arc.png)

Experiment with the [interactive path builder](http://letmespellitoutforyou.com/samples/svg_path.html) by choosing the **A** command and clicking to create new end points. The values of the arc radius, rotation, large-arc, and sweep-arc controls affect the appearance of the last elliptical arc in the path, and apply to newly created arcs.

This summarizes path syntax, with coordinate pairs required for control and destination points:

-   **M**/**m** *destination*: jumps to *destination* point
-   **L**/**l** *destination*: draws straight line to *destination* point
-   **Q**/**q** *control* *destination*: draws quadratic Bézier curve to *destination* point, shaped by *control* point
-   **T**/**t** *destination*: draws quadratic curve to *destination* point, influenced by virtual control point mirroring most recent control point
-   **C**/**c** *control1* *control2* *destination*: draws a cubic Bézier curve to *destination* point, shaped by two control points
-   **S**/**s** *control2* *destination*: draws a cubic Bézier curve to *destination* point, shaped by a virtual control point mirroring the most recent control point, and by a second explicit *control2* point
-   **A**/**a** *radiusX*,*radiusY* *rotationAngle* *large-arc-flag* *sweep-arc-flag* *destination*: draws an elliptical arc to *destination*, if possible, with overall ellipse shaped by *radiusX*,*radiusY* and rotated by *rotationAngle*. The *large-arc-flag* prefers the widest-angle arc path, and *sweep-arc-flag* specifies the ellipse whose arc path travels clockwise to get to the destination point.

## Fill rules

Whenever lines within paths cross each other, and when subpath shapes appear as islands within other shapes, it is not immediately obvious how such paths might be filled. By default, the [**fill-rule**](/w/index.php?title=svg/properties/fill-rule&action=edit&redlink=1) property is set to **nonzero**, which errs on the side of filling regions based on the direction of each stroke, which as the example below shows, may not always be intuitive. Setting it to **evenodd** prevents regions bordering each other from sharing the same fill value.

![svg fillrule nonzero.png](/assets/public/0/01/svg_fillrule_nonzero.png)

    fill-rule: nonzero;

![svg fillrule evenodd.png](/assets/public/b/be/svg_fillrule_evenodd.png)

    fill-rule: evenodd;

Note that while these arrows appear to be separate graphics, they are actually sub-paths. The [**fill-rule**](/w/index.php?title=svg/properties/fill-rule&action=edit&redlink=1) property only applies in this case.

## Markers

You can attach arrowheads or other graphic objects to paths, lines, polylines, and polygon segments. A [**marker**](/svg/elements/marker) element encapsulates a graphic, and various properties reference it. Here is a typical arrowhead, for convenience placed within a [**defs**](/svg/elements/defs) region as a common definition:

``` xml
<defs>
  <marker id="arrowhead" markerWidth="10" markerHeight="10" orient="auto" refX="2" refY="5">
    <polygon points="0,0 10,5 0,10"/>    <!-- triangle pointing right -->
  </marker>
</defs>
```

 The [**marker**](/svg/elements/marker) element does not render unless it is associated with a path or other line element using various marker-related properties. This example places the arrowhead at the end of the last path segment:

``` css
 path.pointer {
     marker-end: url(#arrowhead);
 }
```

 Alternately, the [**marker-start**](/w/index.php?title=svg/properties/marker-start&action=edit&redlink=1) property places the marker at the path's starting point. Setting [**marker-mid**](/w/index.php?title=svg/properties/marker-mid&action=edit&redlink=1) places the marker at each segment point within the path, including where subpaths terminate. The [**marker**](/w/index.php?title=svg/properties/marker&action=edit&redlink=1) property places the graphic at *all* these points:

![svg marker start.png](/assets/public/f/fd/svg_marker_start.png)

    marker-start

![svg marker end.png](/assets/public/d/d0/svg_marker_end.png)

    marker-end

![svg marker mid.png](/assets/public/e/e5/svg_marker_mid.png)

    marker-mid

![svg marker.png](/assets/public/c/c7/svg_marker.png)

    marker

Several [**marker**](/svg/elements/marker) element attributes are necessary to place the arrowhead correctly over the path. By default, the top left corner of the marker graphic is placed over the path or line. Since the graphic is a 10-pixel square in this case, the **refY** attribute moves the point at which it intersects the line down by 5 pixels, in order to center it vertically.

The marker graphic also does not rotate by default to match where the path or line is pointing. Setting [**orient**](/w/index.php?title=svg/attributes/orient&action=edit&redlink=1) to **auto** aligns the graphic's horizontal *x* axis. You can also set [**orient**](/w/index.php?title=svg/attributes/orient&action=edit&redlink=1) to specific degree values. Note in the [**marker-start**](/w/index.php?title=svg/properties/marker-start&action=edit&redlink=1) example above that the initial marker may not be oriented as intended, because it's not associated with an existing line.

## Text

Text behaves much like any other SVG graphic. You can mix text with other graphics, but you can't automatically break lines into blocks of text as in HTML, so you have to set each line independently. Use each [**text**](/svg/elements/text) element's [**x**](/w/index.php?title=svg/attributes/x&action=edit&redlink=1) and [**y**](/w/index.php?title=svg/attributes/y&action=edit&redlink=1) attributes to position its baseline:

``` xml
<text x="100" y="50">The quick brown fox</text>
<text x="100" y="80">jumped over the lazy dog.</text>
```

 ![svg text.png](/assets/thumb/3/31/svg_text.png/400px-svg_text.png)

You can apply standard CSS font properties, along with the [**text-anchor**](/w/index.php?title=css/properties/text-anchor&action=edit&redlink=1) property to center the text from the specified coordinates. You can also control apply [**fill**](/w/index.php?title=svg/properties/fill&action=edit&redlink=1) and [**stroke**](/w/index.php?title=svg/properties/stroke&action=edit&redlink=1) properties just like any other shape:

``` css
text {
    font-family  : Tahoma, sans-serif;
    font-size    : smaller;
    font-weight  : bold;
    text-anchor  : middle;
    fill         : red;
    stroke       : #777;
    stroke-width : 0.5;
}
```

 ![svg textFormatted.png](/assets/thumb/c/ca/svg_textFormatted.png/400px-svg_textFormatted.png)

Use the [**tspan**](/svg/elements/tspan) element to mark and style inline font changes:

``` xml
<text x="100" y="50">The quick brown fox</text>
<text x="100" y="80">
  jumped
     <tspan class="emphasis">over</tspan>
  the lazy dog.
</text>
```

``` css
.emphasis {
    font-style      : italic;
    text-decoration : underline;
}
```

 ![svg textSpan.png](/assets/thumb/d/d6/svg_textSpan.png/400px-svg_textSpan.png)

This example uses the [**dy**](/w/index.php?title=svg/attributes/dy&action=edit&redlink=1) attribute to move text upward to a superscript position and then back down to its original baseline, and [**rotate**](/w/index.php?title=svg/attributes/rotate&action=edit&redlink=1) to spin each character of text. (Applying [**dx**](/w/index.php?title=svg/attributes/dx&action=edit&redlink=1) likewise would displace text horizontally.)

``` xml
<text x="100" y="50">The quick brown fox</text>
<text x="100" y="80">
  jumped
  <tspan rotate="-20" dy="-5">over</tspan>
  <tspan dy="5">the lazy dog.</tspan>
</text>
```

 ![svg textRotate.png](/assets/thumb/1/15/svg_textRotate.png/400px-svg_textRotate.png)

SVG also allows you to place text along the curve of a path. The [**textPath**](/svg/elements/textPath) element diverts any nested text to render along the path it references:

``` xml
<defs>
<path id="curve" d="M 100,300 A 1,1 0 0 1 500,300" />
<text id="textContent">The quick brown fox jumped over the lazy dog.</text>
</defs>
<text>
  <textPath xlink:href="#curve" startOffset="20%">
    <tref xlink:href="#textContent" />
  </textPath>
</text>
```

 The [**tref**](/w/index.php?title=svg/elements/tref&action=edit&redlink=1) element allows you to separately pull in text from a referenced [**text**](/svg/elements/text) element.

The [**textPath**](/svg/elements/textPath)'s [**startOffset**](/w/index.php?title=svg/attributes/startOffset&action=edit&redlink=1) pushes text from the start of the path, disappearing as the path ends. Below the text appears before and after applying the offset:

![svg textPath.png](/assets/thumb/b/b5/svg_textPath.png/400px-svg_textPath.png)

![svg textPathOffset.png](/assets/thumb/9/93/svg_textPathOffset.png/400px-svg_textPathOffset.png)

See [SVG Fonts](/tutorials/svg_fonts) for information on SVG's support for creating font glyphs.
