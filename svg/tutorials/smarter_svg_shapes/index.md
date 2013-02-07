{{Page_Title|Smarter SVG: shapes}}
{{Flags
|High-level issues=Stub
|Editorial notes=[new content from [[User:Sierra|Sierra]] ([[User talk:Sierra|talk]]) -- please do not edit]
}}
{{Byline}}
{{Summary_Section|This guide introduces SVG's basic graphic primitives, from simple lines and shapes to complex polygons and paths.}}
{{Tutorial
|Next_page=[[svg/tutorials/smarter_svg_graphics|Graphics]]
|Prev_page=[[svg/tutorials/smarter_svg_overview|Overview]]
|Content===Simple shapes==

 9 Basic Shapes
    9.1 Introduction
    9.2 The 'rect' element                        {+x y attr}
    9.3 The 'circle' element                      {+cx cy r attr}
    9.4 The 'ellipse' element                     {+rx ry attr}

==Fill and stroke properties==

    11.3 Fill Properties
    11.4 Stroke Properties

* '''fill'''
* '''fill-opacity'''
* '''stroke'''
* '''stroke-width'''
* '''stroke-opacity'''

==Lines and polygons==

    9.5 The 'line' element                        {+ x1 y1 x2 y2 attr}
    9.6 The 'polyline' element                    {+ points attr}
    9.7 The 'polygon' element
        9.7.1 The grammar for points specifications in 'polyline' and 'polygon' elements

==Other properties==

* '''stroke-linecap'''
* '''stroke-linejoin'''
* '''stroke-miterlimit''' (if linejoin:miter)
* '''stroke-dasharray'''
* '''stroke-dashoffset'''
* '''fill-rule'''

==Markers==

    11.6 Markers
        11.6.1 Introduction
        11.6.2 The 'marker' element
        11.6.3 Marker properties
        11.6.4 Details on how markers are rendered

* '''marker'''
* '''marker-end'''
* '''marker-mid'''
* '''marker-start'''

==Paths==

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

([[svg/tutorials/smarter_svg_overview|overview]] /
[[svg/tutorials/smarter_svg_shapes|shapes]] /
[[svg/tutorials/smarter_svg_graphics|graphics]] /
[[svg/tutorials/smarter_svg_text|text]] /
[[svg/tutorials/smarter_svg_filters|filters]] /
[[svg/tutorials/smarter_svg_animation|animation]] /
[[svg/tutorials/smarter_svg_interaction|interaction]])
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