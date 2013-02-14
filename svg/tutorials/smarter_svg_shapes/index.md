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

Rectangles are defined by their '''width''' and '''height'''
attributes, while '''x''' and '''y''' offsets position the
upper-left corner of the '''rect''' relative to its parent:

<syntaxhighlight lang="xml">
<rect x="10" y="10" width="160" height="240"/>
</syntaxhighlight>

Circles are positioned by the '''cx''' and '''cy''' center point,
and the radius ('''r''') specifies the size:

<syntaxhighlight lang="xml">
<circle cx="50" cy="50" r="100"/>
</syntaxhighlight>

Ellipses are positioned like circles, but require two radius attributes:

<syntaxhighlight lang="xml">
<ellipse cx="40" cy="60" rx="40" ry="20"/>
</syntaxhighlight>

When applied to '''rect''' elements, '''rx''' and '''ry''' attributes
provide rounded corners:

<syntaxhighlight lang="xml">
<rect x="10" y="10" width="160" height="240" rx="20" ry="20"/>
</syntaxhighlight>

This
[http://letmespellitoutforyou.com/samples/svg_shapes.html interactive utility]
allows you to manipulate various attributes and see how they apply to
various shapes:

[[Image:svg_shapes.png]]

Use this utility to test lines, polygons, and other CSS properties
described below.

==Fill and stroke properties==

The '''fill''' and '''stroke''' properties specify the color of the
background and the edge of the shape:

<syntaxhighlight lang="xml">
<rect x="10" y="10" width="160" height="240" fill="pink" stroke="red"/>
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

==Other CSS properties==

Additional properties provide greater control over how the ends or
joints of line segments appear. The '''stroke-linecap''' property
determines the appearance of the end of a stroke, or dashes within a
stroke. Options appear as follows, with both '''round''' and
'''square''' extending past the end of the line:

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
and becomes more apparent as the '''stroke-width''' increases:

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
<div style="display:inline-block">
[[Image:svg_linejoin_miterlimit.png]]
 polygon {
   stroke-linejoin   : miter;
   stroke-miterlimit : 2;
   stroke-width      : 10;
 }
</div>

Setting '''stroke-linejoin''' to '''bevel''' diagonally shaves off
sharp protruding angles. Setting it to '''miter''' allows angles to
protrude, but subject to the '''stroke-miterlimit''' property, which
sets the range of protruding pixels at which point the angle is
beveled. (If '''stroke-miterlimit''' is unspecified, there is no
beveling.)

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
''x''/''y'' screen coordinates.

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
one there is an alternative lowercase command that specifies
coordinates in terms relative to the previously defined coordinate.
Starting from the default ''0,0'' origin point, the following path
defines the same shape as the one above:

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

* '''fill-rule'''

==Markers==

<!--
    11.6 Markers
        11.6.1 Introduction
        11.6.2 The 'marker' element
        11.6.3 Marker properties
        11.6.4 Details on how markers are rendered
-->

* '''marker'''
* '''marker-end'''
* '''marker-mid'''
* '''marker-start'''

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