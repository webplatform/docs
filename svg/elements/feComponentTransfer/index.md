---
title: 'feComponentTransfer'
code_samples:
  - 'http://jsfiddle.net/jsfmullany/rtD4A/'
  - 'http://jsfiddle.net/jsfmullany/LPnQ9/'
compatibility:
  feature: feComponentTransfer
  topic: svg
notes:
  - 'Fix broken link to parent'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGComponentTransferElement](/w/index.php?title=svg/objects/SVGComponentTransferElement&action=edit&redlink=1)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'feComponentTransfer is a filter primitive which allows the independent manipulation of each color channel (including the alpha channel) in the input graphic. It is always a child element of a filter element and is the parent of child elements (feFuncR, feFuncG, feFuncB and feFuncA) that perform each color channel manipulation.'
tags:
  - Markup_Elements
  - Graphics
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - svg/objects/SVGComponentTransferElement
uri: svg/elements/feComponentTransfer

---
## Summary

feComponentTransfer is a filter primitive which allows the independent manipulation of each color channel (including the alpha channel) in the input graphic. It is always a child element of a filter element and is the parent of child elements (feFuncR, feFuncG, feFuncB and feFuncA) that perform each color channel manipulation.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGComponentTransferElement](/w/index.php?title=svg/objects/SVGComponentTransferElement&action=edit&redlink=1)

**feComponentTransfer** in combination with its child elements (feFuncR, feFuncG, feFuncB and feFuncA) allows the independent manipulation of each color channel of the input graphic.

Attributes:

-   in (optional): specifies the input graphic. If "in" is ommitted; and feComponentTransfer is the first primitive in a filter, the default value is SourceGraphic. Otherwise, the immediately preceding primitive's result is used as input. Permitted values for "in" are described below.
-   result (optional): creates a reference for the primitive's result that other primitives can use as the value of their "in" attribute.
-   color-interpolation-filters (optional): permitted values are "linearRGB" (default) and "sRGB".
-   x, y, width, height (optional): default to the size of the parent filter region.

Like all filter primitives that accept an input, feComponentTransfer can accept the following values as input via the "in" attribute.

-   SourceGraphic: the target element(image, shape, group etc.) that references the filter
-   SourceAlpha: a graphic containing just the alpha channel of the target element.
-   BackgroundImage: the canvas beneath the SourceGraphic (requires a correctly specified "enable-background" attribute. (limited browser support as of Dec '12)
-   BackgroundAlpha: the alpha channel of the canvas beneath the SourceGraphic (requires a correctly specified "enable-background" attribute. Limited browser support as of Dec '12)
-   FillPaint: a pseudo-graphic equal to the size of the filter region filled with the fill property of the target element (limited browser support as of Dec '12)
-   StrokePaint: a pseudo-graphic equal to the size of the filter region filled with the stroke property of the target element (limited browser support as of Dec '12)
-   Primitive reference: the "result" of another primitive.

feComponentTransfer offers five types of color manipulations:

-   identity: sets the result pixel's color channel value equal to the input value
-   table: maps equal segments of a color channel to output ranges specified by a "tableValues" array
-   discrete: maps equal segments of a color channel to specific output values specified by a "tableValues" array
-   linear: applies a simple linear formula (intercept + slope\*input) to each input pixel's color channel value
-   gamma: applies a gamma function (offset + amplitude\*(input\^exponent)) to each input pixel's color channel value

All color channel values are \*unitized\* into the range [0 -\> 1] before being processed by the filter primitive regardless of the color unit system in use. This means, for example, that values for the gamma exponent greater than 1 will produce darker results (e.g when the exponent is equal to 2 and the input value is equal to 0.5, the output value will be a dark red ( 0.5\^2 =.25).) In contrast, values for the gamma exponent of less than 1 will lighten the result.

By default, color-manipulation operations using feComponentTransfer take place in linearRGB color space. This may produce unwanted results. For example a color inversion may result in a pronounced shift toward lighter tones. If this is not desired, you may explicitly specify a value of "sRGB" for the optional attribute "color-interpolation-filters".

### Table and Discrete Component Transfers

While linear and gamma transfers are readily understandable, Table and Discrete transfers are more complicated. Below is an example fo a table transfer.

``` xml
<feComponentTransfer>
<feFuncR type="table" tableValues="0.0 0.7 0.9 1.0"/>
</feComponentTransfer>
```

 Here, since there are n=4 values in the "tableValues" array, the input color channel is divided into 3 (n-1) equal ranges whose start and end values are:

     0.00 ... 0.33
     0.33 ... 0.66
     0.66 ... 1.00

Values in these ranges are then evenly mapped into the ranges specified in tableValues, which are:

     0.00 ... 0.70
     0.70 ... 0.90
     0.90 ... 1.00

For example, an input pixel whose red value is 0.5 - the midpoint of the second input range (0.33 to 0.66) - is mapped to the midpoint of the second output range (0.70 to 0.90), resulting in an output value for that pixel of 0.80.

The following graphic illustrates how the input ranges are mapped to the output ranges in this example.

![tabletransfer.png](//static.webplatform.org/9/9c/tabletransfer.png)

Note that the start and end values for the input ranges(and their number) are automatically calculated based on the number of values in "tableValues". For example, if tableValues had eleven values, then the input ranges would be calculated as (0.0 -\> 0.1, 0.1 -\> 0.2 etc. through 0.9 -\> 1.0.) There is no capability in SVG 1.1 to customize the start and end values of input ranges.

A similar example for the discrete transfer is as follows:

``` xml
<feComponentTransfer>
<feFuncR type="discrete" tableValues="0.0 0.7 0.0 1.0"/>
</feComponentTransfer>
```

 This time, since there are 4 input values to the "tableValues" array, the primitive divides the input color channel into 4 equal ranges whose start and end values are:

     0.00 ... 0.25
     0.25 ... 0.50
     0.50 ... 0.75
     0.75 ... 1.00

then it maps those input ranges onto the specific values provided by the tableValues array:

     0.00
     0.70
     0.00
     1.00

For example, an input pixel whose red value is 0.375 - the midpoint of the second input range (0.25 to 0.50) - would be mapped to the second value in the output array: 0.70.

The following graphic illustrates how the input segments are mapped to the output segments in a discrete transfer.

![discretetransfer.png](//static.webplatform.org/c/c9/discretetransfer.png)

## Examples

![blue70sfilterexample.png](//static.webplatform.org/1/18/blue70sfilterexample.png)

Example of a table component transfer. The input ranges are mapped onto continuous output ranges.

```


<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="Blue70s" filterUnits="objectBoundingBox" x="0%" y="0%" width="100%" height="100%">
      <feComponentTransfer in="SourceGraphic" result="A">
        <feFuncR type="table" tableValues="0 0.11 0.22 0.34 0.48 0.61 0.72 0.82 0.89 0.95 1"/>
        <feFuncG type="table" tableValues="0 0.08 0.16 0.26 0.38 0.5 0.62 0.73 0.82 0.87 0.9"/>
        <feFuncB type="table" tableValues="0.2 0.34 0.45 0.53 0.58 0.61 0.64 0.71 0.84 1 "/>
      </feComponentTransfer>
</filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#Blue70s)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​
```

</pre>
[View live example](http://jsfiddle.net/jsfmullany/rtD4A/)

![70sposter.png](//static.webplatform.org/2/29/70sposter.png)

Example of a discrete component transfer. The input ranges are mapped onto specific discrete output values.

```


<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="Poster70s" filterUnits="objectBoundingBox" x="0%" y="0%" width="100%" height="100%">
      <feComponentTransfer in="SourceGraphic" result="A">
        <feFuncR type="discrete" tableValues="0.0 1.0 1.0 1.0"/>
        <feFuncG type="discrete" tableValues="0.0 0.5 0.5 0.9"/>
        <feFuncB type="discrete" tableValues="0.0 0.6"/>
      </feComponentTransfer>
    </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#Poster70s)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​
```

</pre>
[View live example](http://jsfiddle.net/jsfmullany/LPnQ9/)

## Notes

### Remarks

This filter primitive performs component-wise remapping of data as follows for every pixel: It allows operations like brightness adjustment, contrast adjustment, color balance, or thresholding. The **feFuncR**, **feFuncG**, **feFuncB**, and**feFuncA** elements can be children of the **feComponentTransfer** element. For more information, see [**SVGFEFuncRElement**](/svg/elements/feFuncR). The calculations are performed on non-premultiplied color values. If the input graphics consist of premultiplied color values, those values are automatically converted into non-premultiplied color values for this operation. (Note that the undoing and redoing of the premultiplication can be avoided if [**feFuncA**](/svg/elements/feFuncA) is the identity transform and all alpha values on the source graphic are set to 1.)

### Syntax

### Members

#### Properties

The **SVGFEComponentTransferElement** object has these properties.

-   [**height**](/svg/properties/height): Gets or sets the height of an element.
-   [**in1**](/svg/properties/in1): Identifies input for the given filter primitive.
-   [**result**](/svg/properties/result): Provides a reference for the output result of a filter.
-   [**width**](/svg/properties/width): Defines the width of an element.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.

## Related specifications

[SVG 1.1](http://www.w3.org/TR/2011/REC-SVG11-20110816/)
:   W3C Recommendation

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

-   [feColorMatrix](/svg/elements/feColorMatrix)

-   **feComponentTransfer**

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

### Related pages

-   [**SVGFEFuncRElement**](/svg/elements/feFuncR)
