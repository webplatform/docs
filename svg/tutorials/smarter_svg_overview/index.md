{{Page_Title|Smarter SVG: Overview}}
{{Flags
|High-level issues=Stub
|Editorial notes=[new content edited offline by Sierra ([[User:Sierra|Sierra]] ([[User talk:Sierra|talk]])); please do not edit]
}}
{{Byline}}

{{Summary_Section|This guide introduces SVG graphics and shows you all
the basics of how to deploy them along with standard web content --
HTML, CSS, and JavaScript -- with which you should already be
familiar.}}

{{Tutorial
|Content=

This section of the guide highlights some notable differences with
those standards, and provides a quick tour of many SVG features that
are covered in more detail in other sections. It focuses on the unique
way you can build complex interactive graphics from reusable
components, and how to flexibly place them within various drawing
areas. As part of a grand tour to get a feel for how SVG markup works,
you'll stroll through an example that shows how to build a pair of
eyes, and how to move them around and make them blink.

[[Image:scr_svg_eyes.png]]

==What is SVG?==

SVG is a standard XML markup format that renders ''Scalable Vector
Graphics'' within web browsers.  Vector graphics are implemented as
pure shapes that can render crisply at any magnification. In contrast,
''raster'' or ''paint''-style images consist of a series of pixels
that may not display well when zoomed at high resolution.

Use SVG if you want to freely interact with portions of a graphic.
Since SVG renders within the browser's DOM, graphic components can be
styled through CSS, manipulated with JavaScript through core APIs, and
can appear comfortably alongside HTML content.

==Deploying SVG==

Until recently, SVG was fairly difficult to incorporate with other web
content, and there are still many challenges. The HTML5 standard
provides a way to insert ''inline'' regions of SVG into HTML files

[[Image:scr_svg_html.png]]

[[Image:scr_svg_css.png]]

[[Image:scr_svg_svg.png]]



<!--

graphics could only be accessed in separate
''.svg'' files

* inline within HTML

* '''background-image''' and '''list-style-image'''

No D&D: 
http://www.vectomatic.org/svg/support-for-native-drag-and-drop

Rule of Boston driving #73. In keeping with Rule #6, 

Basic law of Boston driving: when offered two choices, _always_ pass on
the right when driving on a highway with three or more lanes.  Choose
this "right" approach especially when that lane is about to end, and
especially in heavy rain conditions.

SVG stands for ''''.

It is a cross-browser
standard that allows you to

SVG is a standard that implements scalable ''vector'' graphics for web browsers.

This section provides a basic overview of how how you can use SVG.

drawing surface.
    5.1 Defining an SVG document fragment: the 'svg' element
        5.1.1 Overview
        5.1.2 The 'svg' element
-->

==Adding styles==

<!--
 6 Styling
    6.1 SVG's styling properties
    6.2 Usage scenarios for styling
    6.3 Alternative ways to specify styling properties
    6.4 Specifying properties using the presentation attributes
    6.5 Styling with XSL
    6.6 Styling with CSS
    6.7 Case sensitivity of property names and values
    6.8 Facilities from CSS and XSL used by SVG
    6.9 Referencing external style sheets
    6.10 The 'style' element
    6.11 The 'class' attribute
    6.12 The 'style' attribute
    6.13 Specifying the default style sheet language
    6.14 Property inheritance
    6.15 The scope/range of styles
    6.16 User agent style sheet
    6.17 Aural style sheets
-->

==Grouping elements==

<!--
    5.2 Grouping: the 'g' element
        5.2.1 Overview
        5.2.2 The 'g' element
-->

==Transforms==

<!--
 7 Coordinate Systems, Transformations and Units
    7.1 Introduction
    7.2 The initial viewport
    7.3 The initial coordinate system
    7.4 Coordinate system transformations
    7.5 Nested transformations
    7.6 The 'transform' attribute
    7.7 The 'viewBox' attribute
    7.8 The 'preserveAspectRatio' attribute
    7.9 Establishing a new viewport
    7.10 Units
    7.11 Object bounding box units
    7.12 Intrinsic sizing properties of the viewport of SVG content
    7.13 Geographic coordinate systems
    7.14 The 'svg:transform' attribute
-->

==The viewport and viewbox==

==Referencing content==

<!--

defs


United Health NYSE:UNH 110,618.00 101,364.00

Wellpoint NYSE:WLP 


low-margin business

-->

==How to use the use tag

==Importing content==

<!--
 23 Extensibility
    23.1 Foreign namespaces and private data
    23.2 Embedding foreign object types
    23.3 The 'foreignObject' element
    23.4 An example
    23.5 Adding private elements and attributes to the DTD
-->

==Other==

<!--
 5 Document Structure
    5.3 Defining content for reuse, and the 'defs' element
        5.3.1 Overview
        5.3.2 The 'defs' element
    5.4 The 'desc' and 'title' elements
    5.5 The 'symbol' element
    5.6 The 'use' element
    5.8 Conditional processing
        5.8.1 Conditional processing overview
        5.8.2 The 'switch' element
        5.8.3 The 'requiredFeatures' attribute
        5.8.4 The 'requiredExtensions' attribute
        5.8.5 The 'systemLanguage' attribute
        5.8.6 Applicability of test attributes
    5.9 Specifying whether external resources are required for proper rendering
    5.10 Common attributes
        5.10.1 Attributes common to all elements: 'id' and 'xml:base'
        5.10.2 The 'xml:lang' and 'xml:space' attributes

 21 Metadata
    21.1 Introduction
    21.2 The 'metadata' element
    21.3 An example

 22 Backwards Compatibility

 1 Introduction
    1.1 About SVG
    1.2 SVG MIME type, file name extension and Macintosh file type
    1.3 SVG Namespace, Public Identifier and System Identifier
    1.4 Compatibility with Other Standards Efforts
    1.5 Terminology
    1.6 Definitions

 2 Concepts
    2.1 Explaining the name: SVG
    2.2 Important SVG concepts
    2.3 Options for using SVG in Web pages

 3 Rendering Model
    3.1 Introduction
    3.2 The painters model
    3.3 Rendering Order
    3.4 How groups are rendered
    3.5 How elements are rendered
    3.6 Types of graphics elements
        3.6.1 Painting shapes and text
        3.6.2 Painting raster images
    3.7 Filtering painted regions
    3.8 Clipping, masking and object opacity
    3.9 Parent Compositing

 4 Basic Data Types and Interfaces
    4.1 Syntax
    4.2 Basic data types
    4.3 Real number precision
    4.4 Recognized color keyword names

    11.5 Controlling visibility
-->

* '''display'''
* '''visibility'''

* '''color''', used to provide a potential indirect value (currentColor) for the '''fill''', '''stroke''', '''stop-color''', '''flood-color''' and '''lighting-color''' properties. (The SVG properties which support color allow a color specification which is extended from CSS2 to accommodate color definitions in arbitrary color spaces. See Color profile descriptions.)

[http://svg-mitchallen.blogspot.com/2005/03/morphing-shapes-in-svg.html morphing shapes in svg]

([[svg/tutorials/smarter_svg_overview|Overview]] /
[[svg/tutorials/smarter_svg_shapes|Shapes]] /
[[svg/tutorials/smarter_svg_text|Text]] /
[[svg/tutorials/smarter_svg_graphics|Graphics]] /
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