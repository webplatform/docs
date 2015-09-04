---
title: feSpecularLighting
tags:
  - Markup
  - Elements
  - SVG
readiness: 'In Progress'
notes:
  - 'Needs summary, example, spec reference, standardization status'
uri: svg/elements/feSpecularLighting

---
# feSpecularLighting

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The resulting image is an RGBA image based on the light color. The lighting calculation follows the standard specular component of the [Phong lighting model](http://go.microsoft.com/fwlink/p/?LinkId=226233). The resulting image depends on the light color, light position, and surface geometry of the input bump map.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.25.25

### Members

The **SVGFESpecularLightingElement** object has these properties:

-   [**height**](/svg/properties/height): Gets or sets the height of an element.
-   [**in1**](/svg/properties/in1): Identifies input for the given filter primitive.
-   [**kernelUnitLengthX**](/svg/properties/kernelUnitLengthX): **kernelUnitLength** indicates the intended distance in current filter units for *dx* and *dy* in the surface normal calculation formulas.
-   [**kernelUnitLengthY**](/svg/properties/kernelUnitLengthY): **kernelUnitLength** indicates the intended distance in current filter units for *dx* and *dy* in the surface normal calculation formulas.
-   [**result**](/svg/properties/result): Provides a reference for the output result of a filter.
-   [**specularConstant**](/svg/properties/specularConstant): Specifies the diffuse refection constant used to calculate the effects of diffusion and reflection from a light source.
-   [**surfaceScale**](/svg/properties/surfaceScale): Specifies surface height when the alpha channel of the input image is set to 100% opacity.
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

-   [feGaussianBlur](/svg/elements/feGaussianBlur)

-   [feImage](/svg/elements/feImage)

-   [feMerge](/svg/elements/feMerge)

-   [feMergeNode](/svg/elements/feMergeNode)

-   [feMorphology](/svg/elements/feMorphology)

-   [feOffset](/svg/elements/feOffset)

-   [fePointLight](/svg/elements/fePointLight)

-   **feSpecularLighting**

-   [feSpotlight](/svg/elements/feSpotlight)

-   [feTile](/svg/elements/feTile)

-   [feTurbulence](/svg/elements/feTurbulence)

-   [SVG deployment](/svg/tutorials/smarter_svg_deploy)

-   [SVG filters](/svg/tutorials/smarter_svg_filters)

-   [SVG graphic effects](/svg/tutorials/smarter_svg_graphics)

-   [SVG grand tour](/svg/tutorials/smarter_svg_overview)

-   [SVG filters](/tutorials/svg_filters)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

