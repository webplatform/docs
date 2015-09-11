---
title: feMorphology
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/feMorphology

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## <span>Examples</span>

This example shows a simple text element and two morphology filters applied to the same text. The first filter thins the text with an [**operator**](/svg/properties/operator) value of **erode** and a **radius** value of 1. The second filter thickens the text with an **operator** value of **dilate** and and **radius** value of 1.2.

The image will look like this.

``` html


<!DOCTYPE HTML>
<html>
    <head></head>
    <body>
        <svg width="400" height="400">
            <defs>
                <filter id="MyFilter1" filterUnits="userSpaceOnUse" x="50" y="50" width="300" height="300">
                    <feMorphology operator="erode" radius="1"  />
                </filter>
                <filter id="MyFilter2" filterUnits="userSpaceOnUse" x="50" y="50" width="300" height="300">
                    <feMorphology operator="dilate" radius="1.2"  />
                </filter>
            </defs>
            <g font-family="Verdana" font-size="36" stroke="black" stroke-width="2">
                <text x="50" y="50">
                    Unfiltered
                </text>
                <text x="50" y="150" filter="url(#MyFilter1)">
                    Erode
                </text>
                <text x="50" y="250" filter="url(#MyFilter2)">
                    Dilate
                </text>
            </g>
        </svg>
    </body>
</html>
```

</pre>

## <span>Notes</span>

### <span>Remarks</span>

You can specify thickness or thinness by using the [**operator**](/svg/properties/operator) property.

You can specify how much you what to thicken or thin by using the **radius**, [**radiusX**](/svg/properties/radiusX), and [**radiusY**](/svg/properties/radiusY) properties.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.25.23

### <span>Members</span>

The **SVGFEMorphologyElement** object has these properties:

-   [**height**](/svg/properties/height): Gets or sets the height of an element.
-   [**in1**](/svg/properties/in1): Identifies input for the given filter primitive.
-   [**operator**](/svg/properties/operator): Specifies the operation of whether to thin or thicken.
-   [**radiusX**](/svg/properties/radiusX): Specifies the thickening or thinning you want to apply in the X direction.
-   [**radiusY**](/svg/properties/radiusY): Specifies the thickening or thinning you want to apply in the Y direction.
-   [**result**](/svg/properties/result): Provides a reference for the output result of a filter.
-   [**width**](/svg/properties/width): Defines the width of an element.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.

## <span>See also</span>

### <span>Related articles</span>

#### <span>Filters</span>

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

-   **feMorphology**

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
