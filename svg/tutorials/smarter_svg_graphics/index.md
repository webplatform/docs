{{Page_Title|SVG graphic effects}}
{{Flags
|High-level issues=Stub
|Checked_Out=Yes
}}
{{Byline}}
{{Summary_Section|This guide shows you how to embed images within SVG and apply various graphics effects such as gradients, patterns, clipping paths, and masks.}}
{{Tutorial
|Content===Gradients==

SVG's support for gradients is similar to CSS's. Two kinds of gradient
are available: the
[[svg/elements/linearGradient|'''linearGradient''']] and
[[svg/elements/radialGradient|'''radialGradient''']] elements.  The
[[svg/properties/fill|'''fill''']] property uses '''url()''' syntax to
reference either kind:

<syntaxhighlight lang="xml">
<path id="tvScreen" fill="url(#tvScreenOff)" d="M159.957 184.103c-21.826 13.892-102.52 17.859-122.361 0c-19.843-17.857-22.486-83.999 0-99.873c22.489-15.874 104.504-17.858 122.361 0C177.814 102.088 181.783 170.214 159.957 184.103z"/>
</syntaxhighlight>

This example transitions from a light to a dark gray from the top to
the bottom of the shape:

<syntaxhighlight lang="xml">
<linearGradient id="tvScreenOff" x1="0" y1="0" x2="0" y2="1" >
    <stop offset="0" stop-color="#dddddd" />
    <stop offset="1" stop-color="#444444" />
</linearGradient>
</syntaxhighlight>

[[Image:svg_gfx_gradient_linear_bw.png|200px]]

In their simplest form, gradients require at least two nested
[[svg/elements/stop|'''stop''']] elements to transition between their
[[svg/properties/stop-color|'''stop-color''']] properties. The
[[svg/attributes/offset|'''offset''']] attribute specifies the
progression of colors, either in percentage or corresponding decimal
terms. That progression follows the line defined by the
[[svg/elements/linearGradient|'''linearGradient''']] element's pair of
''x'' and ''y'' coordinates. If '''y1''' were 1 in this example, the
gradient would shift from the top left to the bottom right.

This example defines many more colors, progressing from bottom to top.
Setting [[svg/attributes/gradientUnits|'''gradientUnits''']] to
'''userSpaceOnUse''' makes the ''x''/''y'' coordinates correspond to
specific points within the graphic:

<syntaxhighlight lang="xml">
<linearGradient
   id            = "tvOn"
   x1            = "0"
   y1            = "200"
   x2            = "0"
   y2            = "70"
   gradientUnits = "userSpaceOnUse"
>
    <stop  offset="0"    stop-color="#F15A29" />
    <stop  offset="0.05" stop-color="#F15F29" />
    <stop  offset="0.17" stop-color="#F68D24" />
    <stop  offset="0.32" stop-color="#F9AC1C" />
    <stop  offset="0.42" stop-color="#FCBF13" />
    <stop  offset="0.5"  stop-color="#FDC70C" />
    <stop  offset="1"    stop-color="#1C75BC" />
</linearGradient>
</syntaxhighlight>

[[Image:svg_gfx_gradient_linear.png|200px]]

Radial gradients emanate outwards from the center point by default,
filling rectangular shapes elliptically. In this example, which
generates an obscure cultural reference to an Iggy Pop song, the black
color defined at the 30% mark is extrapolated towards the center at
0%:

<syntaxhighlight lang="xml">
<radialGradient id="tvEye">
  <stop offset="30%"  stop-color="black"     />
  <stop offset="32%"  stop-color="lightblue" />
  <stop offset="58%"  stop-color="lightblue" />
  <stop offset="60%"  stop-color="white"     />
  <stop offset="80%"  stop-color="white"     />
  <stop offset="100%" stop-color="pink"      />
</radialGradient>
</syntaxhighlight>

[[Image:svg_gfx_gradient_radial.png|200px]]

The [[svg/attributes/fx|'''fx''']] and [[svg/attributes/fy|'''fy''']]
attributes specify coordinates for the ''focus'' of the gradient,
while [[svg/attributes/cx|'''cx''']] and
[[svg/attributes/cy|'''cy''']] set the center of the outermost circle.
Modifying the [[svg/attributes/r|'''r''']] (radius) effectively
resizes the gradient, in this case magnifying it relative to the
default 0.5 value:

<syntaxhighlight lang="xml">
<radialGradient id="tvRadial" cx="0.5" cy="0.5" fx="0.8" fy="0.5" r="0.6">
</syntaxhighlight>

[[Image:svg_gfx_gradient_radialY.png|200px]]

[http://letmespellitoutforyou.com/samples/svg/tv_gradient.svg View the SVG file here].

==Patterns==

SVG's patterns are similar to CSS's repeating background images, but
allow you more control over padding and reorienting patterns. To
implement a pattern, you must first design a graphic. In this case, a
rectangle fits within a 5&times;10 area along with a margin of 1 unit:

<syntaxhighlight lang="xml">
<rect id="tileRect" x="0.5" y="0.5" width="9.0" height="4.0" fill="#E1BC9B" />
</syntaxhighlight>

[[Image:svg_gfx_tileRect.png|100px]]

The graphic is wrapped within a [[svg/elements/pattern|'''pattern''']]
element. Its [[svg/attributes/width|'''width''']] and
[[svg/attributes/height|'''height''']] correspond to the intended size
of tile. The [[svg/attributes/x|'''x''']] and
[[svg/attributes/y|'''y''']] simply specify the pattern's offset
starting point.

<syntaxhighlight lang="xml">
<pattern
   id                    = "tilePattern"
   x                     = "0"
   y                     = "0"
   width                 = "10"
   height                = "5"
   patternContentUnits   = "userSpaceOnUse"
   patternUnits          = "userSpaceOnUse"
>
  <use xlink:href="#tileRect" />
</pattern>
</syntaxhighlight>

The units attributes maintain the same fixed coordinate system as for
the overall graphic, so that units are not interpreted as percentages
of the filled object's dimensions.

Use the [[svg/properties/fill|'''fill''']] property to apply the
pattern, in this case to a complex [[svg/elements/path|'''path''']]
shape:

<syntaxhighlight lang="xml">
<path id="headShape" d="M468.054,306.428c0.118,0.623,0.557,0.974,1.042,1.325 ... "/>

<g id="graphic">
  <use xlink:href="#headShape" fill="url(#tilePattern)" />
  <use xlink:href="#shirtShape" />
</g>
</syntaxhighlight>

[[Image:svg_gfx_pattern_rect.png|300px]]

Increasing the pattern's [[svg/attributes/width|'''width''']] and
[[svg/attributes/height|'''height''']] attributes allows you control
over the tile's margins:

[[Image:svg_gfx_pattern_rect_wh.png|300px]]

==More complex tile patterns==

This pattern consists of a very simple shape. You can make the
pattern's nested set of graphics as complex and varied as you want, or
build larger patterns from smaller components. This example shows how
to build series of alternating rotated tiles. First, modify the basic
shape to include black around the margin:

<syntaxhighlight lang="xml">
<g id="tileRect">
  <rect id="tileRectWhite" x="0"   y="0"   width="10"  height="5"   fill="#000000" />
  <rect id="tileRectBlack" x="0.5" y="0.5" width="9.0" height="4.0" fill="#E1BC9B" />
</g>
</syntaxhighlight>

[[Image:svg_gfx_tileRectBlack.png|100px]]

A ''tileSquare'' object duplicates the underlying graphic and uses a
[[svg/attributes/transform|'''transform''']] to move it below the
original to form a 10&times;10 square:

<syntaxhighlight lang="xml">
<g id="tileSquare">
  <use xlink:href="#tileRect" />
  <use xlink:href="#tileRect" transform="translate(0,5)"/>
</g>
</syntaxhighlight>

[[Image:svg_gfx_tileSquare.png|100px]]

The square is then repeated four times within a larger 20&times;20
square:

<syntaxhighlight lang="xml">
<g id="tilePatternUnit">
  <use xlink:href="#tileSquare" />
  <g id="shiftDown" transform="translate(10,10) rotate(90)">
      <use xlink:href="#tileSquare"/>
  </g>
  <g id="shiftOver" transform="translate(10,10) rotate(-90)">
      <use xlink:href="#tileSquare"/>
  </g>
  <g id="shiftDownAndOver" transform="translate(10,10)">
    <use xlink:href="#tileSquare"/>
  </g>
</g>
</syntaxhighlight>

[[Image:svg_gfx_tiles.png|200px]]

All the tiles except for the first one have transforms that move them
to the bottom-right corner of the larger square. The second and third
are rotated, pivoting around their top-left corners so that they
occupy the other two corners.  (Unlike CSS transforms, SVG transforms
do not ''originate'' around the object's center point.)  Rotating by
only 80 degrees may clarify how the transform works:

[[Image:svg_gfx_tiles_rot.png|200px]]

To apply the modified fill, reference the more complex object, and
increase the pattern's tiling area to accomodate it:

<syntaxhighlight lang="xml" highlight="5-6,11">
<pattern
   id                    = "tilePattern"
   x                     = "0"
   y                     = "0"
   width                 = "20"
   height                = "20"
   patternTransform      = "scale(1)"
   patternContentUnits   = "userSpaceOnUse"
   patternUnits          = "userSpaceOnUse"
>
  <use xlink:href="#tilePatternUnit" />
</pattern>
</syntaxhighlight>

[[Image:svg_gfx_pattern.png|300px]]

If the pattern is not sized appropriately for the shape, you do not
have to resize the pattern's dimensions or any of the component tiles.
The example above specifies a
[[svg/attributes/patternTransform|'''patternTransform''']] attribute
with a ''scale(1)'' transform that leaves the size unchanged, but
increasing the value to 1.5 magnifies the pattern:

[[Image:svg_gfx_pattern_scale.png|300px]]

Other transforms allow you to reorient and reshape the pattern. In
this example, ''scale(1.5) skewY(15) rotate(30)'' boosts the pattern's
size, shears it slightly into a diamond shape, and spins it:

[[Image:svg_gfx_pattern_skewrot.png|300px]]

[http://letmespellitoutforyou.com/samples/svg/pattern_fill.svg View the SVG file here].

==Clipping paths==

Patterns are not necessarily for tiny images. By applying generous
[[svg/attributes/width|'''width''']] and
[[svg/attributes/height|'''height''']] pattern dimensions, you can
also use them to display a single large graphic behind an irregular
shape. Another way to do this is to apply a ''clipping path'', which
renders a graphic only inside the contours of another graphic.

Place a [[svg/elements/clipPath|'''clipPath''']] element around the
shape you want to clip the graphic with, in this case the
[[svg/elements/path|'''path''']] we saw earlier that defines the
television screen:

<syntaxhighlight lang="xml">
<clipPath id="screenClip">
    <use xlink:href="#tvScreen"/>
</clipPath>
</syntaxhighlight>

When rendering the graphic to clip, use the
[[svg/properties/clip-path|'''clip-path''']] property to reference the
[[svg/elements/clipPath|'''clipPath''']] element:

<syntaxhighlight lang="xml" highlight="1">
<use xlink:href="#yeller" clip-path="url(#screenClip)" />
<g id="yeller">
  <use xlink:href="#headShape" fill="url(#tilePattern)" />
  <use xlink:href="#shirtShape" />
</g>
</syntaxhighlight>

[[Image:svg_gfx_clip.png|200px]]

[http://letmespellitoutforyou.com/samples/svg/tv_clip.svg View the SVG file here].

==Adding images==

While SVG is designed for vector graphics, it can freely incorporate
raster graphics via the [[svg/elements/image|'''image''']] element.
Use [[svg/attributes/x|'''x''']] and [[svg/attributes/y|'''y''']]
attributes to position an image. Unlike HTML, you need to specify a
[[svg/attributes/width|'''width''']] and
[[svg/attributes/height|'''height''']] for an image to appear:

<syntaxhighlight lang="xml" highlight="1">
<image x="10" y="10" xlink:href="giraffe.png" width="270" height="297"
       preserveAspectRatio="xMidYMid meet"/>
</syntaxhighlight>

If the supplied dimensions don't match the underlying data, various
[[svg/attributes/preserveAspectRatio|'''preserveAspectRatio''']]
options affect the image's placement.  The '''meet''' keyword fits the
entire image, while '''slice''' clips it. To position the image, you
can specify any combination of ''Min'', ''Mid'', and ''Max'', which in
the examples below match for each axis, but which you can mix
arbitrarily. For example, '''xMidYMin''' aligns the image at the top,
and centers it horizontally.  Here are various ways to place a tall
graphic in a wide image container:

<div style="display:inline-block">
 xMinYMin meet
[[Image:xMinYMin_meet.png|300px]]
</div>

<div style="display:inline-block">
 xMidYMid meet
[[Image:xMidYMid_meet.png|300px]]
</div>

<div style="display:inline-block">
 xMaxYMax meet
[[Image:xMaxYMax_meet.png|300px]]
</div>

<div style="display:inline-block">
 xMinYMin slice
[[Image:xMinYMin_slice.png|300px]]
</div>

<div style="display:inline-block">
 xMidYMid slice
[[Image:xMidYMid_slice.png|300px]]
</div>

<div style="display:inline-block">
 xMaxYMax slice
[[Image:xMaxYMax_slice.png|300px]]
</div>

Images scale depending on the current
[[svg/attributes/viewBox|'''viewBox''']]. For example, if the SVG
importing the image appears within a ''viewport'' of 500&times;500
pixels (as specified by its own [[svg/attributes/width|'''width''']]
and [[svg/attributes/height|'''height''']]), but its
[[svg/attributes/viewBox|'''viewBox''']] attribute specifies
'''0 0 1000 1000''', then the image appears much smaller.

You can also use the [[svg/elements/image|'''image''']] element to
import SVG graphics:

<syntaxhighlight lang="xml" highlight="1">
<image xlink:href="face_components.svg#eyes" x="10" y="10" width="300" height="100"/>
</syntaxhighlight>

[[Image:svg_image_import_svg.png]]

These externally referenced SVGs may animate, but do not preserve any
interactive features.

<!--

==Applying masks==

* [[svg/properties/mask|'''mask''']]

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