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

==What are filters?==

A filter is a little machine that takes graphic input, changes it in
some way, and causes the output to render differently. Filters contain
one or more component ''filter effect'' elements, some of which do
intuitively obvious things (such as blur the image), and some of which
only make sense when combined with other effects. (SVG filter effect
elements are all prefixed ''fe''.)

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

Place a [[svg/element/filter|'''filter''']] element within the SVG's
[[svg/element/defs|'''defs''']] region. The
[[svg/element/feGaussianBlur|'''feGaussianBlur''']] element produces a
blurring effect, which matches effect of the
[[css/functions/blur|'''blur()''']] CSS filter function:

<syntaxhighlight lang="xml">
<filter id="blur">
  <feGaussianBlur stdDeviation="10">
</filter>
</syntaxhighlight>

To apply the filter, reference it with the
[[svg/properties/filter|'''filter''']] property, expressed either as
an attribute or via CSS:

<syntaxhighlight lang="xml">
<text class="blurred" filter="url(#blur)" x="30" y="100">An SVG Filter</text>
</syntaxhighlight>

<syntaxhighlight lang="css">
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
<filter id="blur">
  <feGaussianBlur stdDeviation="10 1">
</filter>
</syntaxhighlight>

[[Image:svgf_blur.png]]

If you want to apply this customized SVG filter to HTML content, place
it in an external SVG file and use the corresponding
[[css/properties/filter|'''filter''']] CSS property to reference it
using the same [[css/functions/url|'''url()''']] function:

<syntaxhighlight lang="css">
.sidewaysBlur {
    filter         : url(filters.svg#blur);
    -webkit-filter : url(filters.svg#blur); /* it's a new feature */
}
</syntaxhighlight>

==Modifying colors (feColorMatrix)==

The [[svg/element/feColorMatrix|'''feColorMatrix''']] element provides
several useful ways to modify an image's color. With its
[[svg/attribute/type|'''type''']] set to '''saturate''', reducing the
[[svg/attribute/values|'''values''']] from 1 produces a grayscale,
while increasing it makes the image more vivid, just like the
[[css/functions/saturate|'''saturate()''']] and
[[css/functions/grayscale|'''grayscale()''']] CSS functions:

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="saturate">
  <feColorMatrix type="saturate" values="0"/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXsaturate0.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="saturate">
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
<filter id="hue-rotate">
  <feColorMatrix type="hueRotate" values="180"/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXhurRotate180.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="hue-rotate">
  <feColorMatrix type="luminanceToAlpha"/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXluminanceToAlpha.png|400px]]

</div>

As the name of the [[svg/element/feColorMatrix|'''feColorMatrix''']]
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
[[svg/attribute/values|'''values''']] are stacked here only in the 

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="sepia">
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

___

<!--

====



<syntaxhighlight lang="xml">
<filter id="sepia" >
  <feColorMatrix type="matrix" values=".343 .669 .119 0 0 .249 .626 .130 0 0 .172 .334 .111 0 0 .000 .000 .000 1 0" />
</filter>
</syntaxhighlight>

<syntaxhighlight lang="xml">
<filter id="grayscale">
<feColorMatrix type="matrix"
  values="(0.2126 + 0.7874 * [1 - amount]) (0.7152 - 0.7152 * [1 - amount]) (0.0722 - 0.0722 * [1 - amount]) 0 0
          (0.2126 - 0.2126 * [1 - amount]) (0.7152 + 0.2848 * [1 - amount]) (0.0722 - 0.0722 * [1 - amount]) 0 0
          (0.2126 - 0.2126 * [1 - amount]) (0.7152 - 0.7152 * [1 - amount]) (0.0722 + 0.9278 * [1 - amount]) 0 0
          0 0 0 1 0"/>
</filter>
</syntaxhighlight>

==Modifying pixel components (feComponentTransfer)==



<syntaxhighlight lang="xml">
<filter id="invert">
<feComponentTransfer>
<feFuncR type="table" tableValues="[amount] (1 - [amount])"/>
<feFuncG type="table" tableValues="[amount] (1 - [amount])"/>
<feFuncB type="table" tableValues="[amount] (1 - [amount])"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>



<syntaxhighlight lang="xml">
<filter id="opacity">
<feComponentTransfer>
<feFuncA type="table" tableValues="0 [amount]"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>



<syntaxhighlight lang="xml">
<filter id="brightness">
<feComponentTransfer>
<feFuncR type="linear" slope="[amount]"/>
<feFuncG type="linear" slope="[amount]"/>
<feFuncB type="linear" slope="[amount]"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>



<syntaxhighlight lang="xml">
<filter id="contrast">
<feComponentTransfer>
<feFuncR type="linear" slope="[amount]" intercept="-(0.5 * [amount] + 0.5)"/>
<feFuncG type="linear" slope="[amount]" intercept="-(0.5 * [amount] + 0.5)"/>
<feFuncB type="linear" slope="[amount]" intercept="-(0.5 * [amount] + 0.5)"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

==Drop shadow (feOffset, feMerge, feComposite)==

<syntaxhighlight lang="xml">
<filter id="drop-shadow">
<feGaussianBlur in="[alpha-channel-of-input]" stdDeviation="[radius]"/>
<feOffset dx="[offset-x]" dy="[offset-y]" result="offsetblur"/>
<feFlood flood-color="[color]"/>
<feComposite in2="offsetblur" operator="in"/>
<feMerge>
<feMergeNode/>
<feMergeNode in="[input-image]"/>
</feMerge>
</filter>
</syntaxhighlight>

==A warp effect (feTurbulence, feDisplacementMap, feComposite)==

<syntaxhighlight lang="xml">
<filter id="textFilter" >
  <feTurbulence type="fractalNoise" baseFrequency="0.015" numOctaves="2" result="turbulence_3" data-filterId="3" />
  <feDisplacementMap xChannelSelector="R" yChannelSelector="G" in="SourceGraphic" in2="turbulence_3" scale="45" />
  <feGaussianBlur stdDeviation="10" />
  <feSpecularLighting specularExponent="20" surfaceScale="5">
    <feDistantLight elevation="28" azimuth="220" />
  </feSpecularLighting>
  <feComposite operator="in" in2="inputB" />
  <feComposite operator="arithmetic" k2="1" k3="1" in2="inputB" />
</filter>
</syntaxhighlight>

==Bevel effects (feSpecularLighting)==

==(feDiffuseLighting, feDistantLight)==

<syntaxhighlight lang="xml">
<filter id="pictureFilter" >
  <feColorMatrix type="luminanceToAlpha" />
<feDiffuseLighting diffuseConstant="1" surfaceScale="10" result="diffuse3">
<feDistantLight elevation="28" azimuth="45" /></feDiffuseLighting>
<feComposite operator="in" in2="inputTo_3" />
</filter>
</syntaxhighlight>


___


!!!

http://www.svgbasics.com/filters1.html

http://docs.gimp.org/en/plug-in-convmatrix.html


[[css/functions/blur|'''blur()''']],
[[css/functions/brightness|'''brightness()''']],
[[css/functions/contrast|'''contrast()''']],
[[css/functions/drop-shadow|'''drop-shadow()''']],
[[css/functions/grayscale|'''grayscale()''']],
[[css/functions/hue-rotate|'''hue-rotate()''']],
[[css/functions/invert|'''invert()''']],
[[css/functions/opacity|'''opacity()''']],
[[css/functions/saturate|'''saturate()''']], and
[[css/functions/sepia|'''sepia()''']].  All of these CSS effects can
be defined as SVG filters.

CSS

SVG filters

CSS filters

it may help to distinguish ''SVG filters'' from more recent ''CSS
filters''.

Before focusing on SVG filters, it may help to understand how they compare to

Several kinds of ''filter'' are now available:

* SVG

Applying a filter to a graphic element changes how it renders. Filters
typically

The word ''filter'' has come to


You can use filters to blur images,


Filters

SVG filters are collections of ''filter effects''

==Applying SVG filters in HTML==

==Applying filters in SVG==

* feGaussianBlur: motion blur

* feComponentTransfer
    feFuncR
    feFuncG
    feFuncB
    feFuncA

o feImage: places an image
o feTile

o feBlend

* feOffset
* feFlood: applies fill color

o feMorphology [http://www.cs.auckland.ac.nz/courses/compsci773s1c/lectures/ImageProcessing-html/topic4.htm]

* feTurbulence
* feDisplacementMap
* feComposite
* feColorMatrix
o feConvolveMatrix

* feDiffuseLighting
    light source
* feSpecularLighting
    light source
* feMerge
    feMergeNode
    feMergeNode


==Applying SVG filters with CSS==

==Chained filters==

==Blending channels==

==Filter regions==

==Light sources==

Filter Effects properties:
* [[svg/properties/enable-background|'''enable-background''']]
* '''filter'''
* [[svg/properties/flood-color|'''flood-color''']]
* [[svg/properties/flood-opacity|'''flood-opacity''']]
* [[svg/properties/lighting-color|'''lighting-color''']]

37.10. drop-shadow

15 Filter Effects
15.1 Introduction
15.2 An example
15.3 The 'filter' element
15.4 The 'filter' property
15.5 Filter effects region
15.6 Accessing the background image
15.7 Filter primitives overview
15.7.1 Overview
15.7.2 Common attributes
15.7.3 Filter primitive subregion
15.8 Light source elements and properties
15.8.1 Introduction
15.8.2 Light source 'feDistantLight'
15.8.3 Light source 'fePointLight'
15.8.4 Light source 'feSpotLight'
15.8.5 The 'lighting-color' property
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