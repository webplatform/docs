{{Page_Title|Smarter SVG: graphic effects}}
{{Flags
|High-level issues=Stub
|Editorial notes=[new content edited offline by Sierra ([[User:Sierra|Sierra]] ([[User talk:Sierra|talk]])); please do not edit]
}}
{{Byline}}
{{Summary_Section|This guide shows you how to embed images within SVG and apply various graphics effects such as gradients, patterns, clipping, masking, and compositing.}}
{{Tutorial
|Content=

==Patterns==

[[Image:svg_gfx_pattern.png|300px]]

[[Image:svg_gfx_pattern_scale.png|300px]]

[[Image:svg_gfx_pattern_skewrot.png|300px]]

[[Image:svg_gfx_pattern_wh.png|300px]]

[[Image:svg_gfx_tileRect.png|100px]]

[[Image:svg_gfx_tileSquare.png|100px]]

[[Image:svg_gfx_tiles.png|200px]]

<syntaxhighlight lang="xml">
<rect id="tileRect" x="0.5" y="0.5" width="9.0" height="4.0" fill="#E1BC9B" />
</syntaxhighlight>

<syntaxhighlight lang="xml">
<g id="tileSquare">
  <use xlink:href="#tileRect" />
  <use xlink:href="#tileRect" transform="translate(0,5)"/>
</g>
</syntaxhighlight>

<syntaxhighlight lang="xml">
<g id="tiles">
  <use xlink:href="#tileSquare" />
  <g id="shiftDown" transform="translate(10,10)">
    <g transform="rotate(90)">
      <use xlink:href="#tileSquare"/>
    </g>
  </g>
  <g id="shiftOver" transform="translate(10,10)">
    <g transform="rotate(-90)">
      <use xlink:href="#tileSquare"/>
    </g>
  </g>
  <g id="shiftDownAndOver" transform="translate(10,10)">
    <use xlink:href="#tileSquare"/>
  </g>
</g>
</syntaxhighlight>

<syntaxhighlight lang="xml">
<pattern
   id                    = "kitchenFloor"
   x                     = "0"
   y                     = "0"
   width                 = "20"
   height                = "20"
   patternContentUnits   = "userSpaceOnUse"
   patternUnits          = "userSpaceOnUse"
   patternTransform      = "scale(1.2)"
   data-patternTransform = "scale(1.5) skewY(15) rotate(30)"
>
  <use xlink:href="#tiles" />
</pattern>
</syntaxhighlight>

<syntaxhighlight lang="xml">
</syntaxhighlight>

<syntaxhighlight lang="xml">
</syntaxhighlight>

<syntaxhighlight lang="xml">
</syntaxhighlight>

<syntaxhighlight lang="xml">
</syntaxhighlight>

<syntaxhighlight lang="xml">
</syntaxhighlight>

<!--
    13.3 Patterns
-->

==Images==

<!--
    5.7 The 'image' element
-->

==Gradients==

<!--
 13 Gradients and Patterns
    13.1 Introduction
    13.2 Gradients
        13.2.1 Introduction
        13.2.2 Linear gradients
        13.2.3 Radial gradients
        13.2.4 Gradient stops

Gradient properties:
* '''stop-color'''
* '''stop-opacity'''

-->

==Nesting transforms==

==Compositing==

<!--
 14 Clipping, Masking and Compositing
    14.1 Introduction
    14.2 Simple alpha compositing
* '''opacity'''
-->


==Clipping==

<!--
    14.3 Clipping paths
        14.3.1 Introduction
        14.3.2 The initial clipping path
        14.3.3 The 'overflow' and 'clip' properties
        14.3.4 Clip to viewport vs. clip to 'viewBox'
        14.3.5 Establishing a new clipping path: the 'clipPath' element
        14.3.6 Clipping paths, geometry, and pointer events

Other properties for visual media:
* '''clip''', only applicable to outermost svg element.
* '''clip-path'''
* '''clip-rule'''
* '''overflow''', only applicable to elements which establish a new viewport.

-->

==Masking==

<!--
    14.4 Masking
    14.5 Object and group opacity: the 'opacity' property

* '''mask'''
-->

==Rendering preferences==

...

<!--
    11.7 Rendering properties
        11.7.1 Color interpolation properties: 'color-interpolation' and 'color-interpolation-filters'
        11.7.2 The 'color-rendering' property
        11.7.3 The 'shape-rendering' property
        11.7.4 The 'text-rendering' property
        11.7.5 The 'image-rendering' property
    11.8 Inheritance of painting properties

* '''image-rendering'''
* '''shape-rendering'''
* '''text-rendering'''

Color and Painting properties:

* '''color-interpolation'''
* '''color-interpolation-filters'''
* '''color-profile'''
* '''color-rendering'''

 11 Painting: Filling, Stroking and Marker Symbols
    11.1 Introduction
    11.2 Specifying paint

 12 Color
    12.1 Introduction
    12.2 The 'color' property
    12.3 Color profile descriptions
        12.3.1 Overview of color profile descriptions
        12.3.2 Alternative ways of defining a color profile description
        12.3.3 The 'color-profile' element
        12.3.4 The CSS @color-profile rule
        12.3.5 The 'color-profile' property
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
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}