{{Page_Title|SVG filters}}
{{Flags
|High-level issues=Stub
|Checked_Out=Yes
|Editorial notes=[new content edited offline by Sierra ([[User:Sierra|Sierra]] ([[User talk:Sierra|talk]])); please do not edit]
}}
{{Byline}}
{{Summary_Section|This guide shows you how to build SVG image processing filters to create interesting visual effects. It shows how to apply these effects within an SVG graphic, and how to apply them to HTML content using the [[css/properties/filter|'''filter''']] CSS property. It shows how many pre-built CSS filter functions work, and provides some ideas for other effects you can build yourself in SVG.}}
{{Tutorial
|Content=

==What are filters?==

A filter is a little machine that takes graphic input, changes it in
some way, and causes the output to render differently. Filters contain
one or more component ''filter effects'', some of which do intuitively
obvious things (such as blur the image), and some of which only make
sense when combined with other effects.

Filter effects are often chained together so that one effect's output
becomes another effect's input. Filter effects may also operate on
different inputs that are modified independently of each other, then
combined.

The idea of applying filters to web content originated in SVG, but has
recently been extended to CSS, and it helps to clarify the word's
different meanings.  CSS filters currently come in two flavors:

* Built-in ''filter functions'' provide a series of fairly standard pre-built image processing effects, such as [[css/functions/blur|'''blur()''']] and [[css/functions/grayscale|'''grayscale()''']]. These CSS functions can be chained together to form larger effects, but each one can be represented as an SVG filter.

* In addition to standard two-dimensional image processing features, CSS ''custom filters'' allow you to warp the surface of an element in three dimensions. Custom filters are also known as ''shaders'', either ''vertex'' shaders to warp the surface, or ''fragment'' shaders to modify its pixels.

This guide does not discuss these more recent CSS custom filters, but
does show you how to customize your own SVG filters for use in HTML.

==

==Applying SVG filters within SVG==

<syntaxhightlight lang="xml">
<filter id="blur">
<feGaussianBlur stdDeviation="[radius radius]">
</filter>
</syntaxhightlight>

==Applying SVG filters to HTML==

<syntaxhightlight lang="css">
.blur {
    -webkit-filter: url(filters.svg#blur);
}
</syntaxhightlight>

___

<!--


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

* feImage: places an image
* feBlend
* feOffset
* feTile
* feFlood: applies fill color

* feGaussianBlur: motion blur

* feMorphology [http://www.cs.auckland.ac.nz/courses/compsci773s1c/lectures/ImageProcessing-html/topic4.htm]
* feTurbulence
* feDisplacementMap
* feComposite
* feColorMatrix
* feConvolveMatrix
* feComponentTransfer
    feFuncR
    feFuncG
    feFuncB
    feFuncA
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




37.1. grayscale

<syntaxhightlight lang="xml">
<filter id="grayscale">
<feColorMatrix type="matrix"
values="(0.2126 + 0.7874 * [1 - amount]) (0.7152 - 0.7152 * [1 - amount]) (0.0722 - 0.0722 * [1 - amount]) 0 0
(0.2126 - 0.2126 * [1 - amount]) (0.7152 + 0.2848 * [1 - amount]) (0.0722 - 0.0722 * [1 - amount]) 0 0
(0.2126 - 0.2126 * [1 - amount]) (0.7152 - 0.7152 * [1 - amount]) (0.0722 + 0.9278 * [1 - amount]) 0 0
0 0 0 1 0"/>
</filter>
</syntaxhightlight>

37.2. sepia

<syntaxhightlight lang="xml">
<filter id="sepia">
<feColorMatrix type="matrix"
values="(0.393 + 0.607 * [1 - amount]) (0.769 - 0.769 * [1 - amount]) (0.189 - 0.189 * [1 - amount]) 0 0
(0.349 - 0.349 * [1 - amount]) (0.686 + 0.314 * [1 - amount]) (0.168 - 0.168 * [1 - amount]) 0 0
(0.272 - 0.272 * [1 - amount]) (0.534 - 0.534 * [1 - amount]) (0.131 + 0.869 * [1 - amount]) 0 0
0 0 0 1 0"/>
</filter>
</syntaxhightlight>

37.3. saturate

<syntaxhightlight lang="xml">
<filter id="saturate">
<feColorMatrix type="saturate"
values="(1 - [amount])"/>
</filter>
</syntaxhightlight>

37.4. hue-rotate

<syntaxhightlight lang="xml">
<filter id="hue-rotate">
<feColorMatrix type="hueRotate"
values="[angle]"/>
</filter>
</syntaxhightlight>

37.5. invert

<syntaxhightlight lang="xml">
<filter id="invert">
<feComponentTransfer>
<feFuncR type="table" tableValues="[amount] (1 - [amount])"/>
<feFuncG type="table" tableValues="[amount] (1 - [amount])"/>
<feFuncB type="table" tableValues="[amount] (1 - [amount])"/>
</feComponentTransfer>
</filter>
</syntaxhightlight>

37.6. opacity

<syntaxhightlight lang="xml">
<filter id="opacity">
<feComponentTransfer>
<feFuncA type="table" tableValues="0 [amount]"/>
</feComponentTransfer>
</filter>
</syntaxhightlight>

37.7. brightness

<syntaxhightlight lang="xml">
<filter id="brightness">
<feComponentTransfer>
<feFuncR type="linear" slope="[amount]"/>
<feFuncG type="linear" slope="[amount]"/>
<feFuncB type="linear" slope="[amount]"/>
</feComponentTransfer>
</filter>
</syntaxhightlight>

37.8. contrast

<syntaxhightlight lang="xml">
<filter id="contrast">
<feComponentTransfer>
<feFuncR type="linear" slope="[amount]" intercept="-(0.5 * [amount] + 0.5)"/>
<feFuncG type="linear" slope="[amount]" intercept="-(0.5 * [amount] + 0.5)"/>
<feFuncB type="linear" slope="[amount]" intercept="-(0.5 * [amount] + 0.5)"/>
</feComponentTransfer>
</filter>
</syntaxhightlight>

37.9. blur


37.10. drop-shadow

<syntaxhightlight lang="xml">
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
</syntaxhightlight>

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