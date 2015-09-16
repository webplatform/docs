---
title: feConvolveMatrix
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/feConvolveMatrix

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

**Needs Examples**: This section should include examples.

## Notes

### Remarks

**feConvolveMatrix** applies a matrix convolution filter effect. A convolution combines pixels in the input image with neighboring pixels to produce a resulting image. A wide variety of imaging operations can be achieved through convolutions, including blurring, edge detection, sharpening, embossing, and beveling.

A matrix convolution is based on an *n*-by-*m* matrix (the convolution kernel) which describes how a given pixel value in the input image is combined with its neighboring pixel values to produce a resulting pixel value. Each result pixel is determined by applying the kernel matrix to the corresponding source pixel and its neighboring pixels.

Because they operate on pixels, matrix convolutions are inherently resolution-dependent. To make **feConvolveMatrix** produce resolution-independent results, an explicit value should be provided for either the [**filterRes**](/svg/methods/setFilterRes) attribute on the [**filter**](/svg/elements/filter) element and/or attribute [**kernelUnitLength**](/svg/properties/kernelUnitLengthX).

[**kernelUnitLength**](/svg/properties/kernelUnitLengthX), in combination with the other attributes, defines an implicit pixel grid in the filter effects coordinate system (that is, the coordinate system established by the [**primitiveUnits**](/svg/properties/primitiveUnits) attribute). If the pixel grid established by **kernelUnitLength** is not scaled to match the pixel grid established by attribute [**filterRes**](/svg/methods/setFilterRes) (implicitly or explicitly), then the input image will be temporarily rescaled to match its pixels with **kernelUnitLength**. The convolution happens on the resampled image. After applying the convolution, the image is resampled back to the original resolution.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.25.12

### Members

The **SVGFEConvolveMatrixElement** object has these properties:

-   [**bias**](/svg/properties/bias): Shifts the range of the filter. This allows representation of values that would otherwise be clamped to 0 or 1.
-   [**divisor**](/svg/properties/divisor): Affects the final destination color value of the filter.
-   [**edgeMode**](/svg/properties/edgeMode): Determines how to extend the input image as necessary with color values so that the matrix operations can be applied when the kernel is positioned at or near the edge of the input image.
-   [**height**](/svg/properties/height): Gets or sets the height of an element.
-   [**in1**](/svg/properties/in1): Identifies input for the given filter primitive.
-   [**kernelMatrix**](/svg/properties/kernelMatrix): The list of numbers that make up the kernel matrix for the convolution.
-   [**kernelUnitLengthX**](/svg/properties/kernelUnitLengthX): **kernelUnitLength** indicates the intended distance in current filter units for *dx* and *dy* in the surface normal calculation formulas.
-   [**kernelUnitLengthY**](/svg/properties/kernelUnitLengthY): **kernelUnitLength** indicates the intended distance in current filter units for *dx* and *dy* in the surface normal calculation formulas.
-   [**orderX**](/svg/properties/orderX): Indicates the number of cells in each dimension for [**kernelMatrix**](/svg/properties/kernelMatrix).
-   [**orderY**](/svg/properties/orderY): Indicates the number of cells in each dimension for [**kernelMatrix**](/svg/properties/kernelMatrix).
-   [**preserveAlpha**](/svg/properties/preserveAlpha): Indicates that the convolution will apply to all channels or just the color channels.
-   [**result**](/svg/properties/result): Provides a reference for the output result of a filter.
-   [**targetX**](/svg/properties/targetX): Determines the positioning in X of the convolution matrix relative to a given target pixel in the input image.
-   [**targetY**](/svg/properties/targetY): Determines the positioning in Y of the convolution matrix relative to a given target pixel in the input image.
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

-   **feConvolveMatrix**

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
