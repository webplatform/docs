{{Page_Title|SVG: grand tour}}
{{Flags
|Checked_Out=Yes
}}
{{Byline
|Name=Mike Sierra
}}
{{Summary_Section|This brief guide shows different ways to deploy SVG, either within HTML or as standalone files, with various options to reference CSS and JavaScript.}}
{{Tutorial
|Content=Until recently, SVG was fairly difficult to incorporate with
other web content, and there are still many challenges.  The HTML5
standard provides a way to insert ''inline'' regions of SVG into HTML
files.

[[Image:scr_svg_html.png]]

It translates to this basic HTML markup structure, where CSS and
JavaScript may affect both HTML and SVG content:

<syntaxhighlight lang="xml">
<!DOCTYPE html>
<html>
  <head>
    <link href="styles/html_and_svg.css" rel="stylesheet" />
  </head>
  <body>
    <script defer type="text/javascript" src="js/html_and_svg.js">
    </script>
    <svg>
      <!-- define graphics here -->
    </svg>
  </body>
</html>
</syntaxhighlight>

There are also other ways to do it.  You can reference external SVG
files, and render them interactively within the HTML using either
[[html/elements/iframe|'''iframe''']],
[[html/elements/embed|'''embed''']], or
[[html/elements/object|'''object''']] tags:

<syntaxhighlight lang="xml">
<!DOCTYPE html>
<html>
  <head>
    <link href="styles/html_and_svg.css" rel="stylesheet" />
  </head>
  <body>
    <script defer type="text/javascript" src="js/html_and_svg.js"></script>
    <iframe src=’graphics.svg’></iframe>
    <embed src=’graphics.svg’></embed>
    <object data=’graphics.svg’ type=’image/svg+xml’></object>
  </body>
</html>
</syntaxhighlight>

It's also common to reference external SVG files to present static SVG
graphics via CSS. The example below shows how you might place a
right-aligned navigation arrow within a mobile interface, rendering as
crisply as possible on high-resolution handsets:

[[Image:scr_svg_css.png]]

<syntaxhighlight lang="css">
 a[href] {
     background-image    : url(img/nav_arrow.svg);
     background-position : center 0 right 10px;
     background-size     : contain;
     display             : block;
     min-height          : 2em;
     border-radius       : 0.5em;
     padding             : 0.5em;
 }
</syntaxhighlight>

As you will see, you can also use URL anchors to reference individual
component graphics that are collected within an SVG file. This assigns
a custom bullet shape:

<syntaxhighlight lang="css">
 ul > li {
    list-style-image     : url(img/components.svg#bullet);
 }
</syntaxhighlight>

Less common in practice, SVG files can be viewed as standalone files,
perhaps as the target of a navigation. Any SVG file or
[[svg/elements/svg|'''svg''']] tag region can reference its own set of
CSS and JavaScript, which only applies within the SVG:

[[Image:scr_svg_svg.png]]

This example shows how to embed or reference either CSS or JavaScript
from within an SVG file:

<syntaxhighlight lang="xml">
<?xml version="1.0" standalone="no"?>
  <!-- reference CSS here: -->
<?xml-stylesheet href="css/styles.css" type="text/css"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="700px" height="500px" viewBox="0 0 1000 500">
  <defs>
    <style type="text/css">
        <![CDATA[
            /* embed CSS here */
        ]]>
    </style>
  </defs>
  <script type="application/ecmascript">
      <![CDATA[
          // embed JavaScript here
      ]]>
  </script>
  <!-- or reference JavaScript here: -->
  <script type="application/ecmascript" xlink:href="js/app.js">
  </script>
  <!-- define graphics here -->
</svg>
</syntaxhighlight>

From within an SVG, you can also reference components from other SVG
files. The example that follows shows how you might import a graphic
of a cat from another SVG file, then style it ''calico'' based on
referenced CSS:

[[Image:scr_svg_svg2svg.png]]

<syntaxhighlight lang="xml">
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<?xml-stylesheet href="css/svg_styles.css" type="text/css"?>
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="1000" height="1000">
    <use xlink:href="components.svg#cat" class="calico"/>
</svg>
</syntaxhighlight>

You may also be able to use the
[[svg/elements/foreignObject|'''foreignObject''']] tag to render live
HTML content within an SVG graphic environment. This example uses the
[[svg/elements/switch|'''switch''']] tag to test whether the feature
works, as recognized by the tag's
[[svg/attributes/requiredExtensions|'''requiredExtensions''']]
attribute. If not, it uses fallback [[svg/elements/text|'''text''']]:

[[Image:scr_svg_svg2html.png]]

<syntaxhighlight lang="xml">
<?xml version="1.0" standalone="yes"?>
<svg width="4in" height="3in" version="1.1" xmlns='http://www.w3.org/2000/svg'>
  <desc>use 'switch' to test if foreignObject works, otherwise render fallback 'text' content</desc>
  <switch>
    <foreignObject width="100" height="50" requiredExtensions="http://example.com/SVGExtensions/EmbeddedXHTML">
      <!-- XHTML content goes here -->
      <body xmlns="http://www.w3.org/1999/xhtml">
        <p>Here is a paragraph that requires word wrap</p>
        <iframe src="external.html">...or an iframe...</iframe>
      </body>
    </foreignObject>
    <text font-size="10" font-family="Verdana">
      <tspan x="10" y="10">Here is a paragraph that</tspan>
      <tspan x="10" y="20">requires word wrap.</tspan>
    </text>
  </switch>
</svg>
</syntaxhighlight>

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

    5.5 The 'symbol' element

 5 Document Structure
    5.6 The 'use' element
    5.8 Conditional processing
        5.8.1 Conditional processing overview
        5.8.2 The 'switch' element
        5.8.3 The 'requiredFeatures' attribute
        5.8.4 The 'requiredExtensions' attribute
        5.8.5 The 'systemLanguage' attribute
        5.8.6 Applicability of test attributes
    21.2 The 'metadata' element

    11.5 Controlling visibility

* [[svg/properties/display|'''display''']]
* [[svg/properties/visibility|'''visibility''']]

* [[svg/properties/color|'''color''']], used to provide a potential indirect value (currentColor) for the [[svg/properties/fill|'''fill''']], [[svg/properties/stroke|'''stroke''']], [[svg/properties/stop-color|'''stop-color''']], [[svg/properties/flood-color|'''flood-color''']] and [[svg/properties/lighting-color|'''lighting-color''']] properties. (The SVG properties which support color allow a color specification which is extended from CSS2 to accommodate color definitions in arbitrary color spaces. See Color profile descriptions.)

-->

}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Filters
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}