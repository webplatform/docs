{{Page_Title|SVG filters}}
{{Flags
|High-level issues=Stub
|Checked_Out=Yes
|Editorial notes=[new content edited offline by Sierra ([[User:Sierra|Sierra]] ([[User talk:Sierra|talk]])); please do not edit]
}}
{{Byline}}
{{Summary_Section|This guide shows you how to build SVG image processing filters to create interesting visual effects. It shows how to apply these effects within an SVG graphic, and how to apply them to HTML content using the [[css/properties/filter|'''filter''']] CSS property.}}
{{Tutorial
|Content=

The power of SVG filters is matched by the depth and complexity of
available options. It takes a good deal of practice to master the many
filter effects that are available to you, but hopefully this will help
you understand what's possible.  It starts by showing how modify color
values in ways that often correspond to built-in CSS filter functions.
Then it shows you how to split and merge independent channels

==What are filters?==

A filter is a little machine that takes graphic input, changes it in
some way, and causes the output to render differently. Filters contain
one or more component ''filter effect'' elements, some of which do
intuitively obvious things (such as blur the graphic), and some of
which only make sense when combined with other effects.

Filter effects are often chained together so that one effect's output
becomes another effect's input. Filter effects may also operate on
different inputs that are modified independently of each other, then
combined.

While the idea of applying filters to web content originated in SVG,
it has recently been extended to CSS, so it helps to clarify what
''filter'' means in these different contexts.  CSS filters currently
come in two flavors:

* Built-in ''filter functions'' provide a series of fairly standard pre-built image processing effects, such as [[css/functions/blur|'''blur()''']] and [[css/functions/grayscale|'''grayscale()''']]. These CSS functions can be chained together to form larger effects, but each one can be represented as an SVG filter.

* In addition to standard two-dimensional image processing features, CSS ''custom filters'' allow you to warp the surface of an element in three dimensions. Custom filters are also known as ''shaders'', either ''vertex'' shaders to warp the surface, or ''fragment'' shaders to modify its pixels.

This guide does not discuss these more recent CSS custom filters, but
does show you how to customize your own SVG filters for use in HTML.

==Applying a simple filter (feGaussianBlur)==

Start by placing some text within an SVG graphic:

<syntaxhighlight lang="xml">
<text class="blurred" x="30" y="100">An SVG Filter</text>
</syntaxhighlight>

[[Image:svgf_none.png]]

Place a [[svg/elements/filter|'''filter''']] element within the SVG's
[[svg/elements/defs|'''defs''']] region.  The
[[svg/elements/feGaussianBlur|'''feGaussianBlur''']] element produces a
blurring effect, which matches the effect of the
[[css/functions/blur|'''blur()''']] CSS filter function:

<syntaxhighlight lang="xml">
<filter id="css_blur">
  <feGaussianBlur stdDeviation="10"/>
</filter>
</syntaxhighlight>

(SVG filter effect elements are all prefixed ''fe'', and cannot be
placed outside a [[svg/elements/filter|'''filter''']].)

To apply the filter, reference it with the
[[svg/properties/filter|'''filter''']] property, expressed either as
an attribute or via CSS:

<syntaxhighlight lang="xml" highlight="3">
<text 
  class  = "blurred" 
  filter = "url(#css_blur)" 
  x      = "30" 
  y      = "100"
>An SVG Filter</text>
</syntaxhighlight>

<syntaxhighlight lang="css" highlight="2">
.blurred {
    filter      : url(#blur);
    font-family : sans-serif;
    font-size   : 70px;
    fill        : red;
}
</syntaxhighlight>

[[Image:svgf_blurBoth.png]]

The filter takes each pixel and moves it around randomly from its
original location by a radius specified by the '''stdDeviation'''
value.  Unlike the built-in CSS function, you can specify separate
''x'' and ''y'' values to produce a sideways motion effect that in
this case is a bit more legible:

<syntaxhighlight lang="xml">
<filter id="sideways_blur">
  <feGaussianBlur stdDeviation="10 1"/>
</filter>
</syntaxhighlight>

[[Image:svgf_blur.png]]

If you want to apply this customized SVG filter to HTML content, place
it in an external SVG file and use the corresponding
[[css/properties/filter|'''filter''']] CSS property to reference it
using the same [[css/functions/url|'''url()''']] function:

<syntaxhighlight lang="css">
.sidewaysBlur {
    filter         : url(filters.svg#sideways_blur);
    -webkit-filter : url(filters.svg#sideways_blur); /* it's a new feature */
}
</syntaxhighlight>

==Modifying colors with feComponentTransfer==

The [[svg/elements/feComponentTransfer|'''feComponentTransfer''']]
element allows you to modify each RGBA ''component'' represented in
each pixel. Within the element, nest any combination of
[[svg/elements/feFuncR|'''feFuncR''']],
[[svg/elements/feFuncG|'''feFuncG''']],
[[svg/elements/feFuncB|'''feFuncB''']], and
[[svg/elements/feFuncA|'''feFuncA''']] elements to run different types
of function over each pixel component value. 

Setting the [[svg/attribute/type|'''type''']] of function to
'''identity''' is equivalent to leaving out the function element
altogether, keeping the image on the left unchanged.  Setting it to
'''discrete''' allows you to posterize an image, clustering gradual
color shifts into solid bands based on the step values specified in
[[svg/attribute/tableValues|'''tableValues''']]:

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="no_op">
<feComponentTransfer>
  <feFuncR type="identity"/>
  <feFuncG type="identity"/>
  <feFuncB type="identity"/>
  <feFuncA type="identity"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTnoop.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="posterize">
  <feComponentTransfer>
    <feFuncR type="discrete" 
        tableValues="0 0.2 0.4 0.6 0.8 1"/>
    <feFuncG type="discrete" 
        tableValues="0 0.2 0.4 0.6 0.8 1"/>
    <feFuncB type="discrete" 
        tableValues="0 0.2 0.4 0.6 0.8 1"/>
  </feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTband.png|400px]]

</div>

Setting the [[svg/attribute/type|'''type''']] to '''linear'''
multiples the value [[svg/attribute/slope|'''slope''']] value
(relative to the default '''1'''), then adding an
[[svg/attribute/intercept|'''intercept''']] value if present.

The first example reproduces the effect of the CSS
[[css/functions/brightness|'''brightness()''']] function, flattening
the slope to darken the image. The second increases the slope to
brighten the image, but then drops all values by the same amount,
zeroing out many of them:

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="css_brightness">
<feComponentTransfer>
 <feFuncR type="linear" slope="0.5"/>
 <feFuncG type="linear" slope="0.5"/>
 <feFuncB type="linear" slope="0.5"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTlinear.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="thresholded_brightness">
<feComponentTransfer>
 <feFuncR type="linear" slope="1.5" intercept="-0.3"/>
 <feFuncG type="linear" slope="1.5" intercept="-0.3"/>
 <feFuncB type="linear" slope="1.5" intercept="-0.3"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTlinearIntercept.png|400px]]

</div>

Setting the [[svg/attribute/type|'''type''']] to '''table''' lets you
specify your own linear slope based on two
[[svg/attribute/tableValues|'''tableValues''']].  The first example
behaves like the CSS [[css/functions/opacity|'''opacity()''']]
function.  The second, specifying a negative slope from 1 to 0,
behaves like the CSS [[css/functions/invert|'''invert()''']] function:

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="css_opacity">
<feComponentTransfer>
<feFuncA type="table" tableValues="0 0.5"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTopacity.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="css_invert">
<feComponentTransfer>
  <feFuncR type="table" tableValues="1 0"/>
  <feFuncG type="table" tableValues="1 0"/>
  <feFuncB type="table" tableValues="1 0"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTinvert.png|400px]]

</div>

Setting the [[svg/attribute/type|'''type''']] to '''gamma''' allows
you to perform ''gamma correction'', typically to bring up dark
values. The function applies the following formula to produce a curve:
((''amplitude'' &times; ''value''<sup>''exponent''</sup>) +
''offset''). The first example brightens the green, and the second
uses [[svg/attribute/offset|'''offset''']] to bring down the final
result (the same that [[svg/attribute/intercept|'''intercept''']] does
for the '''linear''' type):

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="gamma_correct">
<feComponentTransfer>
 <feFuncG type="gamma" amplitude="1" exponent="0.5"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTgammaOffset0.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="gamma_correct2">
<feComponentTransfer>
 <feFuncG type="gamma" amplitude="1" exponent="0.5"
          offset="-0.1"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTgamma.png|400px]]

</div>

==Transforming colors with feColorMatrix==

The [[svg/elements/feColorMatrix|'''feColorMatrix''']] element provides
other useful ways to modify an image's color. With its
[[svg/attribute/type|'''type''']] set to '''saturate''', reducing the
[[svg/attribute/values|'''values''']] from 1 produces a grayscale,
while increasing it makes the image more vivid, just like the
[[css/functions/grayscale|'''grayscale()''']] and
[[css/functions/saturate|'''saturate()''']] CSS functions:

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="css_grayscale">
  <feColorMatrix type="saturate" values="0"/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXsaturate0.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="css_saturate">
  <feColorMatrix type="saturate" values="10"/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXsaturate10.png|400px]]

</div>

Setting the [[svg/attribute/type|'''type''']] to '''hueRotate'''
alters the angle along the color wheel, just like the
[[css/functions/hue-rotate|'''hue-rotate()''']] CSS function.  Setting
'''luminanceToAlpha''' (no '''values''' necessary) produces an alpha
channel from bright pixels, useful in producing image masks and other
effects described below.

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="css_hue_rotate">
  <feColorMatrix type="hueRotate" values="180"/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXhurRotate180.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="luminance_mask">
  <feColorMatrix type="luminanceToAlpha"/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXluminanceToAlpha.png|400px]]

</div>

As the name of the [[svg/elements/feColorMatrix|'''feColorMatrix''']]
suggests, setting the [[svg/attribute/type|'''type''']] to
'''matrix''' allows you to transform colors yourself. It specifies a
20-element transform whose rows correspond to red, green, blue, and
alpha channels. This transform leaves the image unchanged:

<div style="display:inline-block">
 1 0 0 0 0
 0 1 0 0 0
 0 0 1 0 0
 0 0 0 1 0  
</div>

The first example below reproduces the effect of the CSS
[[css/functions/sepia|'''sepia()''']] function, while the second
simply reduces green and blue tones. (The
[[svg/attribute/values|'''values''']] are stacked into a table only in
the interest of clarity.)

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="css_sepia">
  <feColorMatrix 
    type="matrix" 
    values=".343 .669 .119 0 0 
            .249 .626 .130 0 0
            .172 .334 .111 0 0
            .000 .000 .000 1 0 "/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXsepia.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="dusk">
  <feColorMatrix 
    type="matrix" 
    values="1.0 0   0   0   0
            0   0.2 0   0   0 
            0   0   0.2 0   0 
            0   0   0   1.0 0 "/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXsunset.png|400px]]

</div>

==Splitting and merging: building a drop shadow with feOffset, feFlood, feComposite, and feMerge==

Filters allow you to accept various graphic inputs, modify them
independently, then combine them. This example reproduces the effect
produced by the CSS [[css/functions/drop-shadow|'''drop-shadow()''']]
function. Stepping through each line and seeing the results as you go
may help you build far more complex effects:

<syntaxhighlight lang="xml">
<filter id="css_drop_shadow">
  <feGaussianBlur stdDeviation="2"  in="SourceAlpha" />
  <feOffset dx="4" dy="6"           result="offsetblur"/>
  <feFlood flood-color="#777"/>
  <feComposite operator="in"        in2="offsetblur"/>
  <feMerge>
    <feMergeNode/>
    <feMergeNode                    in="SourceGraphic"/>
  </feMerge>
</filter>
</syntaxhighlight>

<div style="display:inline-block;max-width:280px;padding:12px">

First we start with an image transparency:

[[Image:svgf_dropNoop.png|192px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

We've already seen the
[[svg/elements/feGaussianBlur|'''feGaussianBlur''']] effect in action,
but in this case it behaves differently.  The optional
[[svg/attribute/in|'''in''']] specifies the '''SourceAlpha''', or all
of its non-transparent pixels. The result of that effect, which is
colored black, is passed to the next
[[svg/elements/feOffset|'''feOffset''']] effect, which simply moves it
down and over:

[[Image:svgf_dropOffsetBlur.png|192px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

The [[svg/elements/feFlood|'''feFlood''']] effect simply produces a
color, specified by its
[[svg/properties/flood-color|'''flood-color''']] property.  The effect
is independent of the graphic we've produced so far, doesn't take any
input from the offset effect, so it renders within the filter's entire
region:

[[Image:svgf_dropFlood.png|192px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

By default, the [[svg/attribute/result|'''result''']] of the flood
becomes the next effect's [[svg/attribute/in|'''in''']] value, so
neither of these attributes needs to be explicitly declared here.  The
[[svg/elements/feComposite|'''feComposite''']] effect applies the
'''in''' composite operation on the portion of the gray fill that
falls within the dropped shadow:

[[Image:svgf_dropComposite.png|192px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

Finally, the [[svg/elements/feMerge|'''feMerge''']] effect combines
the modified version of the graphic with the the original. The first
[[svg/elements/feMergeNode|'''feMergeNode''']] accepts the composite
result by default, and the second specifies the '''SourceGraphic''',
which renders over it for the final effect:

[[Image:svgf_dropMerge.png|192px]]

</div>

==A warp effect (feMorphology, feTurbulence, feDisplacementMap)==

<syntaxhighlight lang="xml">
<filter id="warp" >
  <feMorphology radius="3" operator="dilate" result="text"/>
  <feTurbulence type="fractalNoise" baseFrequency="0.015" numOctaves="1" result="warp" />
  <feDisplacementMap xChannelSelector="R" yChannelSelector="G" in="text" in2="warp" scale="60" />
  <feGaussianBlur stdDeviation="1 2" />
</filter>
</syntaxhighlight>


[[Image:svgf_warpStart.png|192px]]

[[Image:svgf_warpMorph.png|192px]]

[[Image:svgf_warpTurbulence.png|192px]]

[[Image:svgf_warpDisplace.png|192px]]

[[Image:svgf_warpBlur.png|192px]]

==___==

<!--
<div style="display:inline-block">

<syntaxhighlight lang="xml">
</syntaxhighlight>

[[Image:svgf_CT_.png|400px]]

</div>
-->

<!--

==Bevel effects (feSpecularLighting)==

==(feDiffuseLighting, feDistantLight)==

fePointLight, feSpotLight, lighting-color

<syntaxhighlight lang="xml">
<filter id="pictureFilter" >
  <feColorMatrix type="luminanceToAlpha" />
<feDiffuseLighting diffuseConstant="1" surfaceScale="10" result="diffuse3">
<feDistantLight elevation="28" azimuth="45" /></feDiffuseLighting>
<feComposite operator="in" in2="inputTo_3" />
</filter>
</syntaxhighlight>

http://www.svgbasics.com/filters1.html

http://docs.gimp.org/en/plug-in-convmatrix.html

o feImage: places an image
o feTile

o feBlend

o feMorphology [http://www.cs.auckland.ac.nz/courses/compsci773s1c/lectures/ImageProcessing-html/topic4.htm]

* feTurbulence
* feDisplacementMap
o feConvolveMatrix

* feDiffuseLighting

* feSpecularLighting


15.5 Filter effects region

15.6 Accessing the background image

15.8 Light source elements and properties

15.8.1 Introduction



15.9 Filter primitive 'feBlend'
15.10 Filter primitive 'feColorMatrix'
15.11 Filter primitive 'feComponentTransfer'
15.12 Filter primitive 'feComposite'
15.13 Filter primitive 'feConvolveMatrix'
15.14 Filter primitive 'feDiffuseLighting'
15.15 Filter primitive 'feDisplacementMap'
15.16 Filter primitive 'feFlood'
15.17 Filter primitive 'feGaussianBlur'
15.18 Filter primitive 'feImage'
15.19 Filter primitive 'feMerge'
15.20 Filter primitive 'feMorphology'
15.21 Filter primitive 'feOffset'
15.22 Filter primitive 'feSpecularLighting'
15.23 Filter primitive 'feTile'
15.24 Filter primitive 'feTurbulence'
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