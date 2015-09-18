---
title: 'feColorMatrix'
code_samples:
  - 'http://code.webplatform.org/gist/5303882'
  - 'http://code.webplatform.org/gist/5303933'
  - 'http://code.webplatform.org/gist/5303960'
  - 'http://code.webplatform.org/gist/5304023'
  - 'http://code.webplatform.org/gist/5304047'
  - 'http://code.webplatform.org/gist/5304064'
  - 'http://code.webplatform.org/gist/5304095'
  - 'http://code.webplatform.org/gist/5304176'
compatibility:
  feature: feColorMatrix
  topic: svg
notes:
  - 'Fix broken link to parent'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGFEColorMatrixElement](/w/index.php?title=svg/objects/SVGFEColorMatrixElement&action=edit&redlink=1)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'feColorMatrix is an SVG filter primitive that allows the manipulation of color values across color channels. It provides more powerful color manipulation flexibility than CSS shorthand filters. It is always a child element of an SVG filter element. Using feColorMatrix, you can change color saturation, perform hue rotations, selectively adjust alpha values of particular channels, adjust contrast, brightness and more. feColorMatrix does not allow the manipulation of relative color values *within* color channels which is provided by the feComponentTransfer primitive.'
tags:
  - Markup_Elements
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - svg/objects/SVGFEColorMatrixElement
uri: svg/elements/feColorMatrix

---
## Summary

feColorMatrix is an SVG filter primitive that allows the manipulation of color values across color channels. It provides more powerful color manipulation flexibility than CSS shorthand filters. It is always a child element of an SVG filter element. Using feColorMatrix, you can change color saturation, perform hue rotations, selectively adjust alpha values of particular channels, adjust contrast, brightness and more. feColorMatrix does not allow the manipulation of relative color values \*within\* color channels which is provided by the feComponentTransfer primitive.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGFEColorMatrixElement](/w/index.php?title=svg/objects/SVGFEColorMatrixElement&action=edit&redlink=1)

feColorMatrix is a filter primitive that allows the manipulation of color values across color channels. It is always a child element of a [[|filter element](/svg/elements/filter)]. Using feColorMatrix, you can change color saturation, perform hue rotations, selectively adjust alpha values of particular channels, adjust contrast, brightness and more. feColorMatrix does not allow the manipulation of relative color values \*within\* color channels which is provided by the feComponentTransfer primitive.

Attributes:

-   in (optional): specifies the input graphic. If "in" is ommitted; and feColorMatrix is the first primitive in a filter, the default value is SourceGraphic. Otherwise, the immediately preceding primitive's result is used as input. Permitted values for "in" are described below.
-   result (optional): creates a reference for the primitive's result that other primitives can use as the value of their "in" or "in2" attributes.
-   color-interpolation-filters (optional): permitted values are "linearRGB" (default) and "sRGB".
-   x, y, width, height (optional): default to the size of the parent filter region.

Other standard SVG element attributes (style, id, class etc.) may also be added to the element. Like all filter primitives that accept an input, feColorMatrix can accept the following values as input via the "in" attribute.

-   SourceGraphic: the target element(image, shape, group etc.) that references the filter
-   SourceAlpha: a graphic containing just the alpha channel of the target element.
-   BackgroundImage: the canvas beneath the SourceGraphic (requires a correctly specified "enable-background" attribute. (limited browser support as of Dec '12)
-   BackgroundAlpha: the alpha channel of the canvas beneath the SourceGraphic (requires a correctly specified "enable-background" attribute. Limited browser support as of Dec '12)
-   FillPaint: a pseudo-graphic equal to the size of the filter region filled with the fill property of the target element (limited browser support as of Dec '12)
-   StrokePaint: a pseudo-graphic equal to the size of the filter region filled with the stroke property of the target element (limited browser support as of Dec '12)
-   Primitive reference: the "result" of another primitive.

feColorMatrix offers four types of color manipulation: 3 shorthands and a matrix manipulation:

-   saturate: adjusts the saturation of all RGB color channels (the alpha channel is not affected). The permitted value according to the specification is 0-1, but many browsers accept higher values \>1 to allow over-saturation.
-   hueRotate: adjusts the hue of all RGB color channels (the alpha channel is not affected)
-   luminanceToAlpha: discards the alpha channel and replaces it with values equal to the input's luminance. The RGB channels are set to black (0,0,0).
-   matrix: a superset of the shorthands. Allows the value of each channel in the output to be specified from a combination of its existing color and alpha channels.

(It's important to note that manipulations are applied to \*non-pre-multiplied" values\*. This means that alpha adjustments (aka. opacity) are unapplied before calculations are performed. This means, for example, that colors that appear similar same visually on a white background (eg. rgba(255,0,0,.5) and rgba(128,0,0,1) can look very different after a feColorMatrix operation. For example, a "saturate=2" will have no effect on the first color, but dramatically redden the second color.)

By default, color-manipulation operations using feColorMatrix take place in linearRGB color space. This may produce unwanted results. For example a color inversion may result in a pronounced shift toward lighter tones. If this is not desired, you may explicitly specify a value of "sRGB" for the optional attribute "color-interpolation-filters".

## Examples

![desaturate.png](//static.webplatform.org/0/03/desaturate.png)

Example of a feColorMatrix with type="saturate"

```
<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="saturate">
      <feColorMatrix in="SourceGraphic" type="saturate" values=".5" result="A"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#saturate)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​
```

[View live example](http://code.webplatform.org/gist/5303882)

![huerotate.png](//static.webplatform.org/1/19/huerotate.png)

Example of a feColorMatrix with type="hueRotate"

```
<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="hueRotate">
      <feColorMatrix in="SourceGraphic" type="hueRotate" values="45" result="A"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#hueRotate)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​

***
```

[View live example](http://code.webplatform.org/gist/5303933)

![luminancetoalpha.png](//static.webplatform.org/0/01/luminancetoalpha.png)

Example of a feColorMatrix with type="luminanceToAlpha"

```
<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="L2A">
      <feColorMatrix in="SourceGraphic" type="luminanceToAlpha" result="A"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#L2A)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​

***
```

[View live example](http://code.webplatform.org/gist/5303960)

![contrast.png](//static.webplatform.org/8/80/contrast.png)

Example of a feColorMatrix with type="matrix" showing a contrast adjustment

```
<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="matrix-contrast">
      <feColorMatrix in="SourceGraphic" type="matrix" values="1.2 0 0 0 -0.2
                                                              0 1.2 0 0 -0.2
                                                              0 0 1.2 0 -0.2
                                                              0 0 0 1 0"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#matrix-contrast)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​

***
```

[View live example](http://code.webplatform.org/gist/5304023)

![sepia.png](//static.webplatform.org/c/cd/sepia.png)

Example of a feColorMatrix with type="matrix" showing a sepia adjustment

```
<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="matrix-sepia">
      <feColorMatrix in="SourceGraphic" type="matrix" values=".35 .35 .35 0 0
                                                              .25 .25 .25 0 0
                                                              .15 .15 .15 0 0
                                                              0 0 0 1 0"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#matrix-sepia)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​

***
```

[View live example](http://code.webplatform.org/gist/5304047)

![grey.png](//static.webplatform.org/f/fa/grey.png)

Example of a feColorMatrix with type="matrix" showing a standard greyscale adjustment

```
<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="matrix-greyscale">
      <feColorMatrix in="SourceGraphic" type="matrix" values=".33 .33 .33 0 0
                                                              .33 .33 .33 0 0
                                                              .33 .33 .33 0 0
                                                              0 0 0 1 0"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#matrix-greyscale)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​

***
```

[View live example](http://code.webplatform.org/gist/5304064)

![greygreen.png](//static.webplatform.org/8/8c/greygreen.png)

Example of a feColorMatrix with type="matrix" showing a greyscale with green channel weighting

```
<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="matrix-greyscale-greenboost">
      <feColorMatrix in="SourceGraphic" type="matrix" values=".25 .5 .25 0 0
                                                              .25 .5 .25 0 0
                                                              .25 .5 .25 0 0
                                                              0 0 0 1 0"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#matrix-greyscale-greenboost)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​

***
```

[View live example](http://code.webplatform.org/gist/5304095)

![invert.png](//static.webplatform.org/f/f8/invert.png)

Example of a feColorMatrix with type="matrix" showing an inversion

```
<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="matrix-invert">
      <feColorMatrix in="SourceGraphic" type="matrix" values="-1 0 0 0 1
                                                              0 -1 0 0 1
                                                              0 0 -1 0 1
                                                              0 0 0 1 0"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#matrix-invert)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​

***
```

[View live example](http://code.webplatform.org/gist/5304176)

## Notes

### Remarks

This filter applies the following matrix transformation:

    | R' |     | a00 a01 a02 a03 a04 |   | R |
    | G' |     | a10 a11 a12 a13 a14 |   | G |
    | B' |  =  | a20 a21 a22 a23 a24 | * | B |
    | A' |     | a30 a31 a32 a33 a34 |   | A |
    | 1  |     |  0   0   0   0   1  |   | 1 |

This matrix is applied on the RGBA color and alpha values of every pixel on the input graphics to produce a result with a new set of RGBA color and alpha values.

The calculations are performed on non-premultiplied color values. If the input graphics consist of premultiplied color values, those values are automatically converted into non-premultiplied color values for this operation.

### Syntax

### Standards information

-   [SVG 1.1 Specification](http://www.w3.org/TR/SVG/filters.html#feColorMatrixElement)

### Members

The **SVGFEColorMatrixElement** object has these properties:

-   [**height**](/svg/properties/height): Gets or sets the height of an element.
-   [**in1**](/svg/properties/in1): Identifies input for the given filter primitive.
-   [**result**](/svg/properties/result): Provides a reference for the output result of a filter.
-   [**type**](/svg/properties/type_(SVGFEColorMatrixElement)): Indicates the type of matrix operation.
-   [**values**](/svg/properties/values): Numeric values for the **feColorMatrix** transformation matrix.
-   [**width**](/svg/properties/width): Defines the width of an element.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.

## See also

### Related articles

#### Filters

-   [blur()](/css/functions/blur)

-   [brightness()](/css/functions/brightness)

-   [contrast()](/css/functions/contrast)

-   [custom()](/css/functions/custom)

-   [drop-shadow()](/css/functions/drop-shadow)

-   [grayscale()](/css/functions/grayscale)

-   [hue-rotate()](/css/functions/hue-rotate)

-   [invert()](/css/functions/invert)

-   [opacity()](/css/functions/opacity)

-   [saturate()](/css/functions/saturate)

-   [sepia()](/css/functions/sepia)

-   [filter](/css/properties/filter)

-   [feBlend](/svg/elements/feBlend)

-   **feColorMatrix**

-   [feComponentTransfer](/svg/elements/feComponentTransfer)

-   [feComposite](/svg/elements/feComposite)

-   [feConvolveMatrix](/svg/elements/feConvolveMatrix)

-   [feDiffuseLighting](/svg/elements/feDiffuseLighting)

-   [feDisplacementMap](/svg/elements/feDisplacementMap)

-   [feDistantLight](/svg/elements/feDistantLight)

-   [feFlood](/svg/elements/feFlood)

-   [feFuncA](/svg/elements/feFuncA)

-   [feFuncB](/svg/elements/feFuncB)

-   [feFuncG](/svg/elements/feFuncG)

-   [feFuncR](/svg/elements/feFuncR)

-   [feGaussianBlur](/svg/elements/feGaussianBlur)

-   [feImage](/svg/elements/feImage)

-   [feMerge](/svg/elements/feMerge)

-   [feMergeNode](/svg/elements/feMergeNode)

-   [feMorphology](/svg/elements/feMorphology)

-   [feOffset](/svg/elements/feOffset)

-   [fePointLight](/svg/elements/fePointLight)

-   [feSpecularLighting](/svg/elements/feSpecularLighting)

-   [feSpotlight](/svg/elements/feSpotlight)

-   [feTile](/svg/elements/feTile)

-   [feTurbulence](/svg/elements/feTurbulence)

-   [SVG deployment](/svg/tutorials/smarter_svg_deploy)

-   [SVG filters](/svg/tutorials/smarter_svg_filters)

-   [SVG graphic effects](/svg/tutorials/smarter_svg_graphics)

-   [SVG grand tour](/svg/tutorials/smarter_svg_overview)

-   [SVG filters](/tutorials/svg_filters)
