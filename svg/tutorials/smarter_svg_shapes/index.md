{{Page_Title|Smarter SVG: shapes}}
{{Flags
|High-level issues=Stub
|Editorial notes=[new content from Sierra ([[User:Sierra|Sierra]] ([[User talk:Sierra|talk]])); please do not edit]
}}
{{Byline}}
{{Summary_Section|This guide introduces SVG's basic graphic primitives, from simple lines and shapes to complex polygons and paths.}}
{{Tutorial
|Content=

==Simple shapes==

Various SVG elements produce basic shapes, and attributes specify
their dimensions.

Rectangles are defined by their '''width''' and '''height'''
attributes, while '''x''' and '''y''' offsets position the
upper-left corner of the '''rect''' relative to its parent:

<syntaxhighlight lang="xml">
<rect x="10" y="10" width="240" height="160"/>
</syntaxhighlight>

Circles are positioned by the '''cx''' and '''cy''' center point,
and the radius ('''r''') specifies the size:

<syntaxhighlight lang="xml">
<circle cx="50" cy="50" r="100"/>
</syntaxhighlight>

Ellipses are positioned like circles, but require two '''rx''' and
'''ry''' radius attributes for each axis:

<syntaxhighlight lang="xml">
<ellipse cx="40" cy="60" rx="40" ry="20"/>
</syntaxhighlight>

When applied to '''rect''' elements, '''rx''' and '''ry''' attributes
produce rounded corners:

<syntaxhighlight lang="xml">
<rect x="10" y="10" width="160" height="240" rx="20" ry="20"/>
</syntaxhighlight>

This is how these examples appear:

[[Image:svg_shapes.png]]

This
[http://letmespellitoutforyou.com/samples/svg_shapes.html interactive utility]
allows you to manipulate various attributes and see how they apply to
various shapes.  Use it to test lines, polygons, and other CSS
properties described below.

==Fill and stroke properties==

The '''fill''' and '''stroke''' properties specify the color of the
background and the edge of the shape:

<syntaxhighlight lang="xml">
<rect fill="pink" stroke="red" x="10" y="10" width="160" height="240"/>
</syntaxhighlight>

You can assign these as attributes on SVG elements, but they are
really CSS properties. For the sake of clarity, this guide expresses
SVG properties as CSS selectors:

 rect {
     fill   : pink;
     stroke : red;
 }

Properties specified via CSS override those specified as attributes,
so this local CSS that colors the '''rect''' green overrides the local
attribute that colors it red:

<syntaxhighlight lang="xml">
<rect fill="pink" stroke="red" style="fill:lightgreen;stroke:green"
    x="10" y="10" width="160" height="240"/>
</syntaxhighlight>

The '''stroke-width''' is centered over the edge of the shape, so
increasing its pixel value bleeds the '''stroke''' color both inside
and outside the shape:

 rect {
     fill         : pink;
     stroke       : red;
     stroke-width : 6;
 }

To apply transparencies, you can set the '''fill-opacity''' and
'''stroke-opacity''' properties, or specify
[[css/units/color|'''rgba()''' and '''hsla()''']] colors.  Applying
both results in additional transparency:

 rect {
     stroke        : red;
     fill          : rgba(100%,0%,0%,0.5);
     fill-opacity  : 0.5;
     stroke-opacity: 0.5;
     stroke-width  : 6;
 }

==Lines and polygons==

To draw a straight line, specify its start and end coordinates as
'''x1''', '''y1''', '''x2''', and '''y2''':

<syntaxhighlight lang="xml">
<line x1="0" y1="0" x2="100" y2="100"/>
</syntaxhighlight>

A '''polyline''' consists of a series of ''x''/''y'' coordinates
specified within the '''points''' attribute, with items separated by
either commas or whitespace.  This draws an arrow:

<syntaxhighlight lang="xml">
<polyline points="100,225 100,115 130,115 70,15 70,15 10,115 40,115 40,225"/>
</syntaxhighlight>

A '''polygon''' is the same as a '''polyline''', but the final
coordinate is joined with the first:

<syntaxhighlight lang="xml">
<polygon points="100,225 100,115 130,115 70,15 70,15 10,115 40,115 40,225"/>
</syntaxhighlight>

[[Image:svg_polygon.png]]

==Finer control over strokes==

Additional properties provide greater control over how the ends or
joints of line segments appear. The '''stroke-linecap''' property
determines the appearance of the end of a stroke, or dashes within a
stroke. Options appear as follows, with both '''round''' and
'''square''' extending past the end of the line depending on the
'''stroke-width'''::

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

The '''stroke-linejoin''' property affects how joined segments appear,
and becomes more apparent for narrower angles as the
'''stroke-width''' increases:

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

Setting '''stroke-linejoin''' to '''bevel''' diagonally shaves the
points from angles, and setting it to '''miter''' allows them to
protrude.  The '''stroke-miterlimit''' property limits how much of the
angle is allowed to protrude, expressed relative to the
'''stroke-width'''.  This example only bevels those angles that
protrude twice the width:

<div style="display:inline-block">
[[Image:svg_linejoin_miterlimit.png]]
 polygon {
   stroke-linejoin   : miter;
   stroke-miterlimit : 2;
   stroke-width      : 10;
 }
</div>

The '''stroke-dasharray''' property allows you define arbitrary dash
patterns as a comma-separated list of pixel values. A value of
''20,10,10,10'' draws a dash 20 pixels long, followed by a gap of 10
pixels before the following 10-pixel dash, another gap, followed the
same pattern repeated to the end of the shape:

[[Image:svg_stroke_dasharray.png]]

The '''stroke-dashoffset''' property allows you to shift the number of
pixels at which the pattern begins.  As the interactive utility shows,
properties with numeric and color values can be animated and
transitioned with CSS, allowing for potentially distracting marquee
effects.

==Paths==

Paths are complex shapes that may feature discontinuous series of
lines and curves. The '''path''' element's '''d''' (definition)
attribute specifies a sequence of commands referencing pairs of
''x''/''y'' coordinates within the drawing area.

The following
[http://letmespellitoutforyou.com/samples/svg_path.html interactive utility]
allows you to build path definitions using all the commands detailed
below. Choose the command you want, then click within the drawing area
to provide each set of coordinates:

[[Image:svg_path.png]]

The simplest path commands drop a pen at one coordinate and draw a
line to another. In this example, the '''M''' (move) command places
the drawing point at the ''100,225'' coordinate. The '''L''' (line)
command draws a line to ''100,115'', and subsequent '''L''' commands
draw the same arrow-shaped polygon shown above:

<syntaxhighlight lang="xml">
<path d="M 100,225 L 100,115 L 130,115 L 70,15 L 10,115 L 40,115 L 40,225 z"/>
</syntaxhighlight>

The '''z''' command at the end draws a final line to the most recent
'''M''' coordinate to close off the box. At any point along the path,
you may use '''M''' to place the drawing point elsewhere to set off
discontinuous segments known as ''subpaths''.

Coordinates and commands can be separated by any combination of commas
or whitespace characters. (To clarify these examples, commas separate
each coordinate pair.)

The uppercase commands above specify absolute coordinates.  For each
there is an alternative lowercase command that specifies coordinates
in terms relative to the previously defined coordinate.  Starting from
the default ''0,0'' origin point, the following path defines the same
shape as the one above:

<syntaxhighlight lang="xml">
<path d="m 100,225 l 0,-110 l 30,0 l -60,-100 l -60,100 l 30,0 l 0,110 z" />
</syntaxhighlight>

The '''H''' and '''V''' commands, and their '''h''' and '''v'''
alternatives, draw a horizontal or vertical line to the specified
coordinate.

The '''path''' element is distinguished from '''polygon''' and
'''polyline''' in its ability to draw curves. B&eacute;zier curves
require additional ''control point'' coordinates that do not render
but that influence the shape of the curve.

The '''Q''' and '''q''' commands define a ''quadratic'' B&eacute;zier
curve using one control point coordinate followed by another
coordinate where the curve segment ends.

<syntaxhighlight lang="xml">
<path d="M 452,132 Q 254,309 591,396 Q 723,419 675,473"/>
</syntaxhighlight>

The '''C''' and '''c''' commands use two intervening control points
to define a more complex ''cubic'' B&eacute;zier curve.

<syntaxhighlight lang="xml">
<path d="M 432,271 C 304,318 455,385 323,461"/>
</syntaxhighlight>

<!--
(2DO: S/s T/t A )
        8.3.6 The cubic Bézier curve commands     {+c/s}
        8.3.7 The quadratic Bézier curve commands {+q/t}
        8.3.8 The elliptical arc curve commands   {+a}
        8.3.9 The grammar for path data
    8.4 Distance along a path
-->

==Markers==

You can attach arrowheads or other graphic objects to paths, lines,
polylines, and polygon segments. A '''marker''' element encapsulates a
graphic, and various properties reference it. Here is a typical
arrowhead, for convenience placed within a '''defs''' region as a
common definition:

<syntaxhighlight lang="xml">
<defs>
  <marker id="arrowhead" markerWidth="10" markerHeight="10" orient="auto" refX="2" refY="5">
    <!-- triangle pointing right -->
    <polygon points="0,0 10,5 0,10"/>
  </marker>
</defs>
</syntaxhighlight>

The '''marker''' element does not render unless it is associated with
a path or other line element using various marker-related properties.
This example places the arrowhead at the end of the last path segment:

 path.pointer {
     marker-end: url(#arrowhead);
 }

Alternately, the '''marker-start''' property places the marker at the
path's starting point. Setting '''marker-mid''' places the marker at
each segment point within the path, including where subpaths
terminate.  The '''marker''' property places the graphic at ''all''
these points:

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

Several '''marker''' element attributes are necessary to place the
arrowhead correctly over the path. By default, the top left corner of
the marker graphic is placed over the path or line. Since the graphic
is a 10-pixel square in this case, the '''refY''' attribute moves the
point at which it intersects the line down by 5 pixels, in order to
center it vertically.

The marker graphic also does not rotate by default to match where the
path or line is pointing. Setting '''orient''' to '''auto''' aligns
the graphic's horizontal ''x'' axis.  You can also set '''orient''' to
specific degree values. Note in the '''marker-start''' example above
that the initial marker may not be oriented as intended, because it
doesn't extend an existing line.

<!--
2DO:

The '''markerWidth''' and '''markerHeight''' attributes set the ...

* '''markerUnits'''
-->

==Modifying Fills==

<!--
2do:

* '''fill-rule'''
-->

([[svg/tutorials/smarter_svg_overview|Overview]] /
[[svg/tutorials/smarter_svg_shapes|Shapes]] /
[[svg/tutorials/smarter_svg_graphics|Graphics]] /
[[svg/tutorials/smarter_svg_text|Text]] /
[[svg/tutorials/smarter_svg_filters|Filters]] /
[[svg/tutorials/smarter_svg_animation|Animation]] /
[[svg/tutorials/smarter_svg_interaction|Interaction]])

}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}