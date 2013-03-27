{{Page_Title|SVG: basic shapes}}
{{Flags
|High-level issues=Stub
|Checked_Out=Yes
}}
{{Byline}}
{{Summary_Section|This guide introduces SVG's basic graphic elements, from simple lines and shapes to complex polygons and freehand paths.}}
{{Tutorial
|Content=

==Simple shapes==

Various SVG elements produce basic shapes, and attributes specify
their dimensions.

Rectangles are defined by their [[svg/attributes/width|'''width''']]
and [[svg/attributes/height|'''height''']] attributes, while
[[svg/attributes/x|'''x''']] and [[svg/attributes/y|'''y''']] offsets
position the upper-left corner of the [[svg/elements/rect|'''rect''']]
relative to its parent:

<syntaxhighlight lang="xml">
<rect x="10" y="10" width="240" height="160"/>
</syntaxhighlight>

Circles are positioned by the [[svg/attributes/cx|'''cx''']] and
[[svg/attributes/cy|'''cy''']] center point, and the radius
([[svg/attributes/r|'''r''']]) specifies the size:

<syntaxhighlight lang="xml">
<circle cx="50" cy="50" r="100"/>
</syntaxhighlight>

Ellipses are positioned like circles, but require two
[[svg/attributes/rx|'''rx''']] and [[svg/attributes/ry|'''ry''']]
radius attributes for each axis:

<syntaxhighlight lang="xml">
<ellipse cx="40" cy="60" rx="40" ry="20"/>
</syntaxhighlight>

When applied to [[svg/elements/rect|'''rect''']] elements,
[[svg/attributes/rx|'''rx''']] and [[svg/attributes/ry|'''ry''']]
attributes produce rounded corners:

<syntaxhighlight lang="xml">
<rect x="10" y="10" width="160" height="240" rx="20" ry="20"/>
</syntaxhighlight>

This is how these examples appear:

[[Image:svg_shapes.png]]

This
[http://letmespellitoutforyou.com/samples/svg_shapes.html interactive shape-building tool]!
allows you to manipulate various attributes and see how they apply to
corresponding shapes.  Use it to test lines, polygons, and other CSS
properties described below.

==Fill and stroke properties==

By default, shapes are filled black.  The
[[svg/properties/fill|'''fill''']] and
[[svg/properties/stroke|'''stroke''']] properties specify the color of
the background and the edge of the shape.

<syntaxhighlight lang="xml">
<rect fill="pink" stroke="red" x="10" y="10" width="160" height="240"/>
</syntaxhighlight>

You can assign these as attributes on SVG elements, but they are
really CSS properties. For the sake of clarity and best practice, this
guide expresses SVG properties as CSS selectors:

<syntaxhighlight lang="css">
 rect {
     fill   : pink;
     stroke : red;
 }
</syntaxhighlight>

Properties specified via CSS override those specified as attributes,
so this local CSS that colors the [[svg/elements/rect|'''rect''']]
green overrides the local attribute that colors it red:

<syntaxhighlight lang="xml">
<rect fill="pink" stroke="red" style="fill:lightgreen;stroke:green"
    x="10" y="10" width="160" height="240"/>
</syntaxhighlight>

The [[svg/properties/stroke-width|'''stroke-width''']] is centered
over the edge of the shape, so increasing its pixel value bleeds the
[[svg/properties/stroke|'''stroke''']] color both inside and outside
the shape:

<syntaxhighlight lang="css">
 rect {
     fill         : pink;
     stroke       : red;
     stroke-width : 6;
 }
</syntaxhighlight>

To apply transparencies, you can set the
[[svg/properties/fill-opacity|'''fill-opacity''']] and
[[svg/properties/stroke-opacity|'''stroke-opacity''']] properties.

<syntaxhighlight lang="css">
 rect {
     stroke-width   : 10;
     stroke         : red;
     stroke-opacity : 0.5;
     fill           : red;
     fill-opacity   : 0.25;
 }
</syntaxhighlight>

[[Image:svg_opacity.png]]

Alternately, you can use [[css/units/color|'''rgba()''' and
'''hsla()''']] CSS colors to to incorpoarate opacity as part of
[[svg/properties/fill|'''fill''']] and
[[svg/properties/stroke|'''stroke''']] property values. The following
has the same effect as the example above:

<syntaxhighlight lang="css">
 rect {
     stroke-width : 10;
     stroke       : rgba(100%,0%,0%,0.5);
     fill         : rgba(100%,0%,0%,0.25);
 }
</syntaxhighlight>

==Lines and polygons==

To draw a straight line, specify its start and end coordinates as
'''x1''', '''y1''', '''x2''', and '''y2''':

<syntaxhighlight lang="xml">
<line x1="0" y1="0" x2="100" y2="100"/>
</syntaxhighlight>

A [[svg/elements/polyline|'''polyline''']] consists of a series of
''x''/''y'' coordinates specified within the
[[svg/attributes/points|'''points''']] attribute, with items separated
by either commas or whitespace.  This draws an arrow:

<syntaxhighlight lang="xml">
<polyline points="100,225 100,115 130,115 70,15 70,15 10,115 40,115 40,225"/>
</syntaxhighlight>

A [[svg/elements/polygon|'''polygon''']] is the same as a
[[svg/elements/polyline|'''polyline''']], but the final coordinate is
joined with the first:

<syntaxhighlight lang="xml">
<polygon points="100,225 100,115 130,115 70,15 70,15 10,115 40,115 40,225"/>
</syntaxhighlight>

[[Image:svg_linepath.png]]

==More stroke properties==

Additional properties provide greater control over how the ends or
joints of line segments appear. The
[[svg/properties/stroke-linecap|'''stroke-linecap''']] property
determines the appearance of the end of a stroke, or dashes within a
stroke. Options appear as follows, with both '''round''' and
'''square''' extending past the end of the line depending on the
[[svg/properties/stroke-width|'''stroke-width''']]::

<div style="display:inline-block">
[[Image:svg_linecap_round.png]]
 stroke-linecap: round;
</div>
<div style="display:inline-block">
[[Image:svg_linecap_square.png]]
 stroke-linecap: square;
</div>
<div style="display:inline-block">
[[Image:svg_linecap_butt.png]]
 stroke-linecap: butt;
</div>

The [[svg/properties/stroke-linejoin|'''stroke-linejoin''']] property
affects how joined segments appear, and becomes more apparent for
narrower angles as the
[[svg/properties/stroke-width|'''stroke-width''']] increases:

<div style="display:inline-block">
[[Image:svg_linejoin_round.png]]
 stroke-linejoin: round;
</div>
<div style="display:inline-block">
[[Image:svg_linejoin_bevel.png]]
 stroke-linejoin: bevel;
</div>
<div style="display:inline-block">
[[Image:svg_linejoin_miter.png]]
 stroke-linejoin: miter;
</div>

Setting [[svg/properties/stroke-linejoin|'''stroke-linejoin''']] to
'''bevel''' diagonally shaves the points from angles, and setting it
to '''miter''' allows them to protrude.  The
[[svg/properties/stroke-miterlimit|'''stroke-miterlimit''']] property
limits how much of the angle is allowed to protrude, expressed
relative to the [[svg/properties/stroke-width|'''stroke-width''']].
This example only bevels those angles that protrude twice the width:

<div style="display:inline-block">
[[Image:svg_linejoin_miterlimit.png]]
 polygon {
   stroke-linejoin   : miter;
   stroke-miterlimit : 2;
   stroke-width      : 10;
 }
</div>

The [[svg/properties/stroke-dasharray|'''stroke-dasharray''']]
property allows you define arbitrary dash patterns as a
comma-separated list of pixel values. A value of ''20,10,10,10'' draws
a dash 20 pixels long, followed by a gap of 10 pixels before the
following 10-pixel dash, another gap, followed the same pattern
repeated to the end of the shape:

[[Image:svg_stroke_dasharray.png]]

 stroke-dasharray: 20,10,10,10;

The [[svg/properties/stroke-dashoffset|'''stroke-dashoffset''']]
property allows you to shift the number of pixels at which the pattern
begins.  As the interactive utility shows, properties with numeric and
color values can be animated and transitioned with CSS, allowing for
potentially distracting marquee effects.

==Simple paths==

Paths are complex shapes that may feature discontinuous series of
lines and curves. The [[svg/elements/path|'''path''']] element's
[[svg/attributes/d|'''d''']] (definition) attribute specifies a
sequence of commands referencing pairs of ''x''/''y'' coordinates
within the drawing area.

The following
[http://letmespellitoutforyou.com/samples/svg_path.html interactive path-building utility]
allows you to create your own path definitions using all the commands
detailed below, and see them reflected in SVG code. Choose the command
you want, then click within the drawing area to provide each set of
coordinates:

[[Image:svg_path.png|600px]]

The simplest path commands drop a pen at one coordinate and draw a
line to another. In this example, the '''M''' (move) command places
the drawing point at the ''100,225'' coordinate. The '''L''' (line)
command draws a line to ''100,115'', and subsequent '''L''' commands
draw the same arrow-shaped polygon shown above, starting from its
bottom-left corner and drawing in a clockwise direction:

<syntaxhighlight lang="xml">
<path d="M 100,225 L 100,115 L 130,115 L 70,15 L 10,115 L 40,115 L 40,225 z"/>
</syntaxhighlight>

[[Image:svg_linepath.png]]

The '''z''' command at the end draws a final line to the most recent
'''M''' coordinate to close off the box. At any point along the path,
you may use '''M''' to place the drawing point elsewhere to set off
discontinuous segments known as ''subpaths''.

Coordinates and commands can be separated by any combination of commas
or whitespace characters. (To clarify these examples, commas separate
each coordinate pair.)

The uppercase '''M''' and '''L''' commands above specify absolute
coordinates.  For all uppercase commands described in this section,
there are alternative lowercase commands that specify coordinates in
terms relative to the previously defined coordinate.  Starting from
the default ''0,0'' origin point, the following path defines the same
shape as the one above using '''m''' and '''l''' commands:

<syntaxhighlight lang="xml">
<path d="m 100,225 l 0,-110 l 30,0 l -60,-100 l -60,100 l 30,0 l 0,110 z" />
</syntaxhighlight>

The '''H''' and '''V''' commands, and their '''h''' and '''v'''
alternatives, draw a horizontal or vertical line to the specified
coordinate.

==Curved paths==

Unlike polygons, paths can incorporate curves.  B&eacute;zier curves
require additional ''control point'' coordinates that do not render
but that influence the shape of the curve.

The '''Q''' and '''q''' commands define a ''quadratic'' B&eacute;zier
curve using one control point coordinate followed by another
coordinate where the curve segment ends. The '''C''' and '''c'''
commands use two intervening control points to define a more complex
''cubic'' B&eacute;zier curve. These examples show where each control
point falls:

<div style="display:inline-block">

[[Image:svg_quadratic.png]]

<syntaxhighlight lang="xml">
<path d="M 50,100 Q 180,20 300,130"/>
</syntaxhighlight>

</div>
<div style="display:inline-block">

[[Image:svg_cubic.png]]

<syntaxhighlight lang="xml">
<path d="M 50,120 C 130,50 250,150 280,100"/>
</syntaxhighlight>

</div>

Adding additional sets of controls points has the same effect as
adding additional '''Q'''/'''q'''/'''C'''/'''c''' commands. The
following definition pairs produce the same sequence of quadratic and
cubic curves, but the second line leaves out the redundant command:

[[Image:svg_quadratic_poly.png]]

<syntaxhighlight lang="xml">
<path d="M 50,100 Q 180,20 300,130 Q 320,20 400,50"/>
<path d="M 50,100 Q 180,20 300,130   320,20 400,50"/>
</syntaxhighlight>

[[Image:svg_cubic_poly.png]]

<syntaxhighlight lang="xml">
<path d="M 50,120 C 130,50 250,150 280,100 C 250,50 450,50 400,100"/>
<path d="M 50,120 C 130,50 250,150 280,100   250,50 450,50 400,100"/>
</syntaxhighlight>

In both of these examples, the curve segments join abruptly at an
angle. The '''T''' and '''t''' commands are designed to produce
quadratic curves that transition smoothly from the previous curve.
They work by extrapolating a control point from the previous control
point on the other side of the previous destination point, effectively
mirroring it to produce waves. The following two path definitions
produce the same sequence of curves. The first uses the '''T'''
command to extrapolate the extra control point (marked red), while the
second uses a second '''Q''' command to explicitly define it.  Both
specify the same destination point:

<syntaxhighlight lang="xml">
<path d="M 50,100 Q 180,20 300,130 T         400,50"/>
<path d="M 50,100 Q 180,20 300,130 Q 420,240 400,50"/>
</syntaxhighlight>

[[Image:svg_quadratic_smooth.png]]

The '''S''' and '''s''' commands perform the same kind of mirroring to
produce smooth cubic B&eacute;zier curves suitable for freehand
drawing.  Since B&eacute;zier curves are defined by two control
points, the first supplied coordinate specifies the second control
point, and the second coordinate specifies the end point.  The
following two path definitions produce the same sequence of curves,
the second substituting the '''C''' command to explicitly define the
extra control point, again marked red:

<syntaxhighlight lang="xml">
<path d="M 50,120 C 130,50 250,150 280,100 S        450,50 400,100"/>
<path d="M 50,120 C 130,50 250,150 280,100 C 310,50 450,50 400,100"/>
</syntaxhighlight>

[[Image:svg_cubic_smooth.png]]

The '''A''' and '''a''' commands specify an ''elliptical arc'', using
syntax specifying a surprisingly great deal of information:

* A pair of radius measurements defining the ellipse's size and shape, equivalent to the [[svg/elements/ellipse|'''ellipse''']] element's [[svg/attributes/rx|'''rx''']] and [[svg/attributes/ry|'''ry''']] attributes.

* A measurement indicating the degree to which the ellipse is rotated.

* A ''large-arc'' flag (''0'' or ''1'') indicating whether to travel to the destination point via the longer arc that exceeds 180&deg;.

* To distinguish between the two possible arcs that mirror each other along the line to the destination point, a ''sweep-arc'' flag (''0'' or ''1'') specifies whether to prefer whichever renders in a clockwise direction.

* A final set of coordinates indicates the ellipse's end point.

If the ellipse's radii is insufficient or if its rotation makes it
impossible to get to the final end point, the ellipse does not render.

[[Image:svg_arc.png|300px]]

Experiment with the
[http://letmespellitoutforyou.com/samples/svg_path.html interactive
path builder] by choosing the '''A''' command and clicking to create
new end points.  The values of the arc radius, rotation, large-arc,
and sweep-arc controls affect the appearance of the last elliptical
arc in the path, and apply to newly created arcs.

This summarizes path syntax, with coordinate pairs required for
control and destination points:

* '''M'''/'''m''' ''destination'': jumps to ''destination'' point
* '''L'''/'''l''' ''destination'': draws straight line to ''destination'' point
* '''Q'''/'''q''' ''control'' ''destination'': draws quadratic B&eacute;zier curve to ''destination'' point, shaped by ''control''
* '''T'''/'''t''' ''destination'': draws quadratic curve to ''destination'' point, influenced by virtual control point mirroring most recent control point
* '''C'''/'''c''' ''control1'' ''control2'' ''destination'': draws a cubic B&eacute;zier curve to ''destination'' point, shaped by two control points
* '''S'''/'''s''' ''control2'' ''destination'': draws a cubic B&eacute;zier curve to ''destination'' point, shaped by a virtual control point mirroring the most recent control point, and by a second ''control2'' point
* '''A'''/'''a''' ''radiusX'',''radiusY'' ''rotationAngle'' ''large-arc-flag'' ''sweep-arc-flag'' ''destination'': draws an elliptical arc to ''destination'', if possible, with overall ellipse shaped by ''radiusX'',''radiusY'' and rotated by ''rotationAngle''. The ''large-arc-flag'' prefers the widest-angle arc path, and ''sweep-arc-flag'' specifies the ellipse whose arc path is clockwise.

==Markers==

You can attach arrowheads or other graphic objects to paths, lines,
polylines, and polygon segments. A
[[svg/elements/marker|'''marker''']] element encapsulates a graphic,
and various properties reference it. Here is a typical arrowhead, for
convenience placed within a [[svg/elements/defs|'''defs''']] region as
a common definition:

<syntaxhighlight lang="xml">
<defs>
  <marker id="arrowhead" markerWidth="10" markerHeight="10" orient="auto" refX="2" refY="5">
    <polygon points="0,0 10,5 0,10"/>    <!-- triangle pointing right -->
  </marker>
</defs>
</syntaxhighlight>

The [[svg/elements/marker|'''marker''']] element does not render
unless it is associated with a path or other line element using
various marker-related properties.  This example places the arrowhead
at the end of the last path segment:

<syntaxhighlight lang="css">
 path.pointer {
     marker-end: url(#arrowhead);
 }
</syntaxhighlight>

Alternately, the [[svg/properties/marker-start|'''marker-start''']]
property places the marker at the path's starting point. Setting
[[svg/properties/marker-mid|'''marker-mid''']] places the marker at
each segment point within the path, including where subpaths
terminate.  The [[svg/properties/marker|'''marker''']] property places
the graphic at ''all'' these points:

<div style="display:inline-block">
[[Image:svg_marker_start.png]]
 marker-start
</div>
<div style="display:inline-block">
[[Image:svg_marker_end.png]]
 marker-end
</div>
<div style="display:inline-block">
[[Image:svg_marker_mid.png]]
 marker-mid
</div>
<div style="display:inline-block">
[[Image:svg_marker.png]]
 marker
</div>

Several [[svg/elements/marker|'''marker''']] element attributes are
necessary to place the arrowhead correctly over the path. By default,
the top left corner of the marker graphic is placed over the path or
line. Since the graphic is a 10-pixel square in this case, the
'''refY''' attribute moves the point at which it intersects the line
down by 5 pixels, in order to center it vertically.

The marker graphic also does not rotate by default to match where the
path or line is pointing. Setting
[[svg/attributes/orient|'''orient''']] to '''auto''' aligns the
graphic's horizontal ''x'' axis.  You can also set
[[svg/attributes/orient|'''orient''']] to specific degree values. Note
in the [[svg/properties/marker-start|'''marker-start''']] example
above that the initial marker may not be oriented as intended, because
it's not associated with an existing line.

<!--
2DO:

The [[svg/attributes/markerWidth|'''markerWidth''']] and
[[svg/attributes/markerHeight|'''markerHeight''']] attributes set the
...

* [[svg/attributes/markerUnits|'''markerUnits''']]
-->

==Fill rules==

Whenever lines within paths cross each other, and when subpath shapes
appear as islands within other shapes, it is not immediately obvious
how such paths might be filled. By default, the
[[svg/properties/fill-rule|'''fill-rule''']] property is set to
'''nonzero''', which errs on the side of filling regions based on the
direction of each stroke, which as the example below shows, may not
always be intuitive. Setting it to '''evenodd''' prevents regions
bordering each other from sharing the same fill value.

<div style="display:inline-block">
[[Image:svg_fillrule_nonzero.png]]
 fill-rule: nonzero;
</div>
<div style="display:inline-block">
[[Image:svg_fillrule_evenodd.png]]
 fill-rule: evenodd;
</div>

Note that while these arrows appear to be separate graphics, they are
actually sub-paths.  The [[svg/properties/fill-rule|'''fill-rule''']]
property only applies in this case.