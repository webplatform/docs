---
title: color
tags:
  - Data
  - Type
  - CSS
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The <color> CSS data type allows for various ways of specifying a color, some of which also specify opacity.'
uri: 'css/data types/color'

---
# \<color\>

## Summary

The \<color\> CSS data type allows for various ways of specifying a color, some of which also specify opacity.

### Syntax

Several different ways are available to specify simple color values:

-   *Keyword* values specify common color names such as **yellow**, **black**, or **transparent**. (See the table below.)

-   Hexadecimal values specify opaque colors in the range of **\#000000** (**black**) to **\#ffffff** (**white**), where each pair of characters correspond to red, green, and blue.

-   An `rgb()` function specifies red, green and blue values either as integers between 0 and 255 (corresponding to the hex values above), or as percentages. For example, `rgb(256,0,0)` and `rgb(100%,0%,0%)` both correspond to **red**.

-   An `hsl()` function specifies hue, saturation, and luminance values. Hue values are specified as an [angle within the color wheel](/css/data_types/angle) relative to **red'*, and numeric values default to degrees. Saturation specifies vividness as a percentage, with****0%**specifying various shades of gray. Luminence specifies brightness, with**0%**and**100%* corresponding to **black** and **white**, and **50%** appearing as a more vivid hue. For example, `hsl(0%,100%,50%)` also corresponds to **red**.

The following variations on the above allow you to incorporate an *alpha* channel specifying transparencies:

-   An `rgba()` function specifies red, green and blue values as described above, along with opacity expressed in decimal terms between 0 and 1. For example, `rgba(100%,0%,0%,0.5)` specifies a semi-transparent red, which would appear as pink if layered over a white background.

-   An `hsla()` function specifies hue, saturation, and luminance as described above, but with an additional *alpha* channel. For example, `hsla(0%,100%,50%,0.5)` specifies the same semi-transparent red as the `rgba()` example above.

The recently introduced **transparent** color name specifies a full transparency.

### Color Keywords

.

<dl data-table="wikitable">
<dt>
Example

</dt>
<dd>
Name

</dd>
<dt>
Example

</dt>
<dd>
aliceblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
antiquewhite

</dd>
<dt>
Non-visible-example

</dt>
<dd>
aqua

</dd>
<dt>
Non-visible-example

</dt>
<dd>
aquamarine

</dd>
<dt>
Non-visible-example

</dt>
<dd>
azure

</dd>
<dt>
Non-visible-example

</dt>
<dd>
beige

</dd>
<dt>
Non-visible-example

</dt>
<dd>
bisque

</dd>
<dt>
Non-visible-example

</dt>
<dd>
black

</dd>
<dt>
Non-visible-example

</dt>
<dd>
blanchedalmond

</dd>
<dt>
Non-visible-example

</dt>
<dd>
blue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
blueviolet

</dd>
<dt>
Non-visible-example

</dt>
<dd>
brown

</dd>
<dt>
Non-visible-example

</dt>
<dd>
burlywood

</dd>
<dt>
Non-visible-example

</dt>
<dd>
cadetblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
chartreuse

</dd>
<dt>
Non-visible-example

</dt>
<dd>
chocolate

</dd>
<dt>
Non-visible-example

</dt>
<dd>
coral

</dd>
<dt>
Non-visible-example

</dt>
<dd>
cornflowerblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
cornsilk

</dd>
<dt>
Non-visible-example

</dt>
<dd>
crimson

</dd>
<dt>
Non-visible-example

</dt>
<dd>
cyan

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkcyan

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkgoldenrod

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkgray

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkgreen

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkgrey

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkkhaki

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkmagenta

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkolivegreen

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkorange

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkorchid

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkred

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darksalmon

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkseagreen

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkslateblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkslategray

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkslategrey

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkturquoise

</dd>
<dt>
Non-visible-example

</dt>
<dd>
darkviolet

</dd>
<dt>
Non-visible-example

</dt>
<dd>
deeppink

</dd>
<dt>
Non-visible-example

</dt>
<dd>
deepskyblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
dimgray

</dd>
<dt>
Non-visible-example

</dt>
<dd>
dimgrey

</dd>
<dt>
Non-visible-example

</dt>
<dd>
dodgerblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
firebrick

</dd>
<dt>
Non-visible-example

</dt>
<dd>
floralwhite

</dd>
<dt>
Non-visible-example

</dt>
<dd>
forestgreen

</dd>
<dt>
Non-visible-example

</dt>
<dd>
fuchsia

</dd>
<dt>
Non-visible-example

</dt>
<dd>
gainsboro

</dd>
<dt>
Non-visible-example

</dt>
<dd>
ghostwhite

</dd>
<dt>
Non-visible-example

</dt>
<dd>
gold

</dd>
<dt>
Non-visible-example

</dt>
<dd>
goldenrod

</dd>
<dt>
Non-visible-example

</dt>
<dd>
gray

</dd>
<dt>
Non-visible-example

</dt>
<dd>
green

</dd>
<dt>
Non-visible-example

</dt>
<dd>
greenyellow

</dd>
<dt>
Non-visible-example

</dt>
<dd>
grey

</dd>
<dt>
Non-visible-example

</dt>
<dd>
honeydew

</dd>
<dt>
Non-visible-example

</dt>
<dd>
hotpink

</dd>
<dt>
Non-visible-example

</dt>
<dd>
indianred

</dd>
<dt>
Non-visible-example

</dt>
<dd>
indigo

</dd>
<dt>
Non-visible-example

</dt>
<dd>
ivory

</dd>
<dt>
Non-visible-example

</dt>
<dd>
khaki

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lavender

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lavenderblush

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lawngreen

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lemonchiffon

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightcoral

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightcyan

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightgoldenrodyellow

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightgray

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightgreen

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightgrey

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightpink

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightsalmon

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightseagreen

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightskyblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightslategray

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightslategrey

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightsteelblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lightyellow

</dd>
<dt>
Non-visible-example

</dt>
<dd>
lime

</dd>
<dt>
Non-visible-example

</dt>
<dd>
limegreen

</dd>
<dt>
Non-visible-example

</dt>
<dd>
linen

</dd>
<dt>
Non-visible-example

</dt>
<dd>
magenta

</dd>
<dt>
Non-visible-example

</dt>
<dd>
maroon

</dd>
<dt>
Non-visible-example

</dt>
<dd>
mediumaquamarine

</dd>
<dt>
Non-visible-example

</dt>
<dd>
mediumblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
mediumorchid

</dd>
<dt>
Non-visible-example

</dt>
<dd>
mediumpurple

</dd>
<dt>
Non-visible-example

</dt>
<dd>
mediumseagreen

</dd>
<dt>
Non-visible-example

</dt>
<dd>
mediumslateblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
mediumspringgreen

</dd>
<dt>
Non-visible-example

</dt>
<dd>
mediumturquoise

</dd>
<dt>
Non-visible-example

</dt>
<dd>
mediumvioletred

</dd>
<dt>
Non-visible-example

</dt>
<dd>
midnightblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
mintcream

</dd>
<dt>
Non-visible-example

</dt>
<dd>
mistyrose

</dd>
<dt>
Non-visible-example

</dt>
<dd>
moccasin

</dd>
<dt>
Non-visible-example

</dt>
<dd>
navajowhite

</dd>
<dt>
Non-visible-example

</dt>
<dd>
navy

</dd>
<dt>
Non-visible-example

</dt>
<dd>
oldlace

</dd>
<dt>
Non-visible-example

</dt>
<dd>
olive

</dd>
<dt>
Non-visible-example

</dt>
<dd>
olivedrab

</dd>
<dt>
Non-visible-example

</dt>
<dd>
orange

</dd>
<dt>
Non-visible-example

</dt>
<dd>
orangered

</dd>
<dt>
Non-visible-example

</dt>
<dd>
orchid

</dd>
<dt>
Non-visible-example

</dt>
<dd>
palegoldenrod

</dd>
<dt>
Non-visible-example

</dt>
<dd>
palegreen

</dd>
<dt>
Non-visible-example

</dt>
<dd>
paleturquoise

</dd>
<dt>
Non-visible-example

</dt>
<dd>
palevioletred

</dd>
<dt>
Non-visible-example

</dt>
<dd>
papayawhip

</dd>
<dt>
Non-visible-example

</dt>
<dd>
peachpuff

</dd>
<dt>
Non-visible-example

</dt>
<dd>
peru

</dd>
<dt>
Non-visible-example

</dt>
<dd>
pink

</dd>
<dt>
Non-visible-example

</dt>
<dd>
plum

</dd>
<dt>
Non-visible-example

</dt>
<dd>
powderblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
purple

</dd>
<dt>
Non-visible-example

</dt>
<dd>
red

</dd>
<dt>
Non-visible-example

</dt>
<dd>
rosybrown

</dd>
<dt>
Non-visible-example

</dt>
<dd>
royalblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
saddlebrown

</dd>
<dt>
Non-visible-example

</dt>
<dd>
salmon

</dd>
<dt>
Non-visible-example

</dt>
<dd>
sandybrown

</dd>
<dt>
Non-visible-example

</dt>
<dd>
seagreen

</dd>
<dt>
Non-visible-example

</dt>
<dd>
seashell

</dd>
<dt>
Non-visible-example

</dt>
<dd>
sienna

</dd>
<dt>
Non-visible-example

</dt>
<dd>
silver

</dd>
<dt>
Non-visible-example

</dt>
<dd>
skyblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
slateblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
slategray

</dd>
<dt>
Non-visible-example

</dt>
<dd>
slategrey

</dd>
<dt>
Non-visible-example

</dt>
<dd>
snow

</dd>
<dt>
Non-visible-example

</dt>
<dd>
springgreen

</dd>
<dt>
Non-visible-example

</dt>
<dd>
steelblue

</dd>
<dt>
Non-visible-example

</dt>
<dd>
tan

</dd>
<dt>
Non-visible-example

</dt>
<dd>
teal

</dd>
<dt>
Non-visible-example

</dt>
<dd>
thistle

</dd>
<dt>
Non-visible-example

</dt>
<dd>
tomato

</dd>
<dt>
Non-visible-example

</dt>
<dd>
turquoise

</dd>
<dt>
Non-visible-example

</dt>
<dd>
violet

</dd>
<dt>
Non-visible-example

</dt>
<dd>
wheat

</dd>
<dt>
Non-visible-example

</dt>
<dd>
white

</dd>
<dt>
Non-visible-example

</dt>
<dd>
whitesmoke

</dd>
<dt>
Non-visible-example

</dt>
<dd>
yellow

</dd>
<dt>
Non-visible-example

</dt>
<dd>
yellowgreen

</dd>
</dl>
## Examples

``` {.css}
aside {
    color: white;              /* white letterforms */
    text-shadow: 0 0 4px red;  /* red backlight effect */
    text-shadow: 0 0 4px rgb(100%, 0%, 0%);  /* same */
    background-color: #777777; /* gray background */
}
.semitrans {
    /* elements behind this show through */
    background-color: rgba(50%, 50%, 50%, 0.5);
}
```

## Related specifications

Specification
:   Status
[CSS Values and Units Module Level 3](http://www.w3.org/TR/css3-values/)
:   Candidate Recommendation
[CSS Color Module Level 3](http://www.w3.org/TR/2011/REC-css3-color-20110607/)
:   Recommendation
[CSS 2.1](http://www.w3.org/TR/CSS21/syndata.html#color-units)
:   Recommendation

## See also

### Other articles

-   [Setting color in CSS](/tutorials/setting_color_in_css)
-   [color](/css/color)
-   [color](/css/properties/color)

