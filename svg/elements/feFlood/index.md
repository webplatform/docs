---
title: 'feFlood'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: feFlood
  topic: svg
notes:
  - 'Needs summary, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/feFlood

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

This example shows a simple flood filter that is green colored and has an opacity of 50%.

The image will look like this.

``` html


<!DOCTYPE HTML>
<html>
    <head></head>
    <body>
        <svg width="400" height="400">
            <defs>
               <filter id="MyFilter" filterUnits="userSpaceOnUse" x="0" y="0"  width="400" height="400">
                  <feFlood x="100" y="100" width="100" height="100"
                    flood-color="green" flood-opacity="0.5"/>
               </filter>
            </defs>
            <use filter="url(#MyFilter)" x='0' y='0'/>
            </svg>
    </body>
</html>
```

</pre>

## Notes

### Remarks

The purpose of this filter is to provide a rectangular area that can be part of a larger filter chain. If you do not supply a color or opacity, the default values will be used. You can supply the [**x**](/svg/properties/x), [**y**](/svg/properties/y), [**width**](/svg/properties/width), and [**height**](/svg/properties/height) values, but if you do not, they will be defined by the general filter region.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.25.18

### Members

The **SVGFEFloodElement** object has these properties:

-   [**height**](/svg/properties/height): Gets or sets the height of an element.
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

-   [feDiffuseLighting](/svg/elements/feDiffuseLighting)

-   [feDisplacementMap](/svg/elements/feDisplacementMap)

-   [feDistantLight](/svg/elements/feDistantLight)

-   **feFlood**

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
