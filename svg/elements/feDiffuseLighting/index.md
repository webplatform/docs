---
title: 'feDiffuseLighting'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: feDiffuseLighting
  topic: svg
notes:
  - 'Needs summary, example, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
tags:
  - Markup_Elements
  - SVG
  - Needs_Summary
  - Needs_Examples
uri: svg/elements/feDiffuseLighting

---
## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Notes

### Remarks

The resulting image is an RGBA opaque image based on the light color where alpha = 1.0. The lighting calculation follows the standard diffuse component of the [Phong lighting model](http://go.microsoft.com/fwlink/p/?LinkId=226233). The resulting image depends on the light color, the light position, and the surface geometry of the input bump map.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.25.13

### Members

The **SVGFEDiffuseLightingElement** object has these properties:

-   [**diffuseConstant**](/svg/properties/diffuseConstant): Defines the diffuse reflection constant.
-   [**height**](/svg/properties/height): Gets or sets the height of an element.
-   [**in1**](/svg/properties/in1): Identifies input for the given filter primitive.
-   [**kernelUnitLengthX**](/svg/properties/kernelUnitLengthX): **kernelUnitLength** indicates the intended distance in current filter units for *dx* and *dy* in the surface normal calculation formulas.
-   [**kernelUnitLengthY**](/svg/properties/kernelUnitLengthY): **kernelUnitLength** indicates the intended distance in current filter units for *dx* and *dy* in the surface normal calculation formulas.
-   [**result**](/svg/properties/result): Provides a reference for the output result of a filter.
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

-   **feDiffuseLighting**

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
