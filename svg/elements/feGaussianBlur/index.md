---
title: 'feGaussianBlur'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: feGaussianBlur
  topic: svg
notes:
  - 'Needs summary, example, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/feGaussianBlur

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The Gaussian blur kernel is an approximation of the normalized convolution

G(x,y) = H(x)I(y),

where

H(x) = exp(-x<sup>2</sup>/ (2s<sup>2</sup>)) / sqrt(2\* pi\*s<sup>2</sup>)

and

I(y) = exp(-y<sup>2</sup>/ (2t<sup>2</sup>)) / sqrt(2\* pi\*t<sup>2</sup>)

with 's' being the standard deviation in the x direction and 't' being the standard deviation in the y direction, as specified by the [**stdDeviationX**](/svg/properties/stdDeviationX) and [**stdDeviationY**](/svg/properties/stdDeviationY) properties.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.25.19

### Members

The **SVGFEGaussianBlurElement** object has these methods:

-   [**setStdDeviation**](/svg/methods/setStdDeviation): Sets the standard deviation values used in calculating a Gaussian blur.

The **SVGFEGaussianBlurElement** object has these properties:

-   [**height**](/svg/properties/height): Gets or sets the height of an element.
-   [**in1**](/svg/properties/in1): Identifies input for the given filter primitive.
-   [**result**](/svg/properties/result): Provides a reference for the output result of a filter.
-   [**stdDeviationX**](/svg/properties/stdDeviationX): Gets a value that indicates the standard deviation in the x-direction, used in calculating a Gaussian blur.
-   [**stdDeviationY**](/svg/properties/stdDeviationY): Gets a value that indicates the standard deviation in the y-direction, used in calculating a Gaussian blur.
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

-   [feColorMatrix](/svg/elements/feColorMatrix)

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

-   **feGaussianBlur**

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
