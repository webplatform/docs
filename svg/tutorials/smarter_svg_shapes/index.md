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
<circle cx="50" cy="50" r="100"></circle>
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

==Fill and stroke properties==

The '''fill''' and '''stroke''' properties specify the color of the
background and the edge of the shape:

<syntaxhighlight lang="xml">
<rect x="10" y="10" width="160" height="240" fill="pink" stroke="red"/>
</syntaxhighlight>

You can assign these as attributes on SVG elements, but they are
really CSS properties. Throughout this guide, properties that apply to
SVG elements are shown in style sheets:

 rect {
     fill   : pink;
     stroke : red;
 }

Properties specified via CSS clobber those specified as attributes, so
this '''rect''' is green:

<syntaxhighlight lang="xml">
<rect fill="pink" stroke="red" style="fill:lightgreen;stroke:green" x="10" y="10" width="160" height="240"/>
</syntaxhighlight>

The '''stroke-width''' is centered over the edge of the shape, so
increasing it bleeds the '''stroke''' color both inside and outside
the shape:

<syntaxhighlight lang="xml">
<rect fill="pink" stroke="red" stroke-width="6" x="10" y="10" width="160" height="240"/>
</syntaxhighlight>

To apply transparencies, you can set the '''fill-opacity''' and
'''stroke-opacity''' properties, or specify
[[css/units/color|'''rgba()''' and '''hsla()''']] colors.  Applying
both results in extra transparency:

<syntaxhighlight lang="xml">
<rect stroke="red" fill="rgba(100%,0%,0%,0.5)" fill-opacity="0.5" stroke-opacity="0.5" stroke-width="6" x="10" y="10" width="160" height="240"/>
</syntaxhighlight>

==Lines and polygons==

To draw a line, specify its start and end coordinates as '''x1''',
'''y1''', '''x2''', and '''y2''':

<syntaxhighlight lang="xml">
<line x1="0" y1="0" x2="100" y2="100"/>
</syntaxhighlight>

A '''polyline''' is a series of ''x''/''y'' coordinates listed in the
'''points''' attribute, separated by either commas or whitespace. This
draws an arrow:

<syntaxhighlight lang="xml">
<polyline points="100,225 100,115 130,115 70,15 70,15 10,115 40,115 40,225"/>
</syntaxhighlight>

A '''polygon''' is the same as a '''polyline''', but the last
coordinate is joined with the first:

<syntaxhighlight lang="xml">
<polygon points="100,225 100,115 130,115 70,15 70,15 10,115 40,115 40,225"/>
</syntaxhighlight>

==Other properties==

* '''stroke-linecap'''
* '''stroke-linejoin'''
* '''stroke-miterlimit''' (if linejoin:miter)
* '''stroke-dasharray'''
* '''stroke-dashoffset'''
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

==Paths==

<!--
 8 Paths
    8.1 Introduction
    8.2 The 'path' element                        {+ d attr}
    8.3 Path data
        8.3.1 General information about path data
        8.3.2 The "moveto" commands               {+m}
        8.3.3 The "closepath" command             {+z}
        8.3.4 The "lineto" commands               {+l/h/v x,y;x;y}
        8.3.5 The curve commands
        8.3.6 The cubic Bézier curve commands     {+c/s}
        8.3.7 The quadratic Bézier curve commands {+q/t}
        8.3.8 The elliptical arc curve commands   {+a}
        8.3.9 The grammar for path data
    8.4 Distance along a path
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