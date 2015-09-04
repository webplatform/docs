---
title: feFuncB
tags:
  - Markup
  - Elements
  - SVG
readiness: 'Not Ready'
notes:
  - 'Merge candidate; see feFuncA.'
uri: svg/elements/feFuncB

---
# feFuncB

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

**Needs Examples**: This section should include examples.

## Notes

### Remarks

This topic describes the **feFuncR**, **feFuncG**, **feFuncB**, and **feFuncA** elements. These four elements are typically children of [**feComponentTransferelement**](/svg/elements/feComponentTransfer) and specify the transfer functions for the four channels, as follows:

-   **feFuncR** — transfer function for the red component of the input graphic
-   **feFuncG** — transfer function for the green component of the input graphic
-   **feFuncB** — transfer function for the blue component of the input graphic
-   **feFuncA** — transfer function for the alpha component of the input graphic

The following rules apply to the processing of the [**feComponentTransferelement**](/svg/elements/feComponentTransfer) element:

-   If more than one transfer function element of the same kind is specified, the last occurrence is used.
-   If any of the transfer function elements are unspecified, the [**feComponentTransferelement**](/svg/elements/feComponentTransfer) must be processed as if those transfer function elements were specified with their **type** attributes set to **identity** (see below).

In addition to core attributes (**id**, **xml:base**, **xml:lang**, and **xml:space**), the following seven attributes are applicable to the **feFuncR**, **feFuncG**, **feFuncB** and **feFuncA** elements:

-   **type**

The **type** attribute can be one of five values: **identity**, **table**, **discrete**, **linear**, or **gamma** (see below). These five values indicate the type of component transfer function. The value of **type** determines the applicability of the other attributes (as discussed below).

In the following, C is the initial component (such as **feFuncR**), C' is the re-mapped component; both in the closed interval [0, 1]:

-   -   For **identity**:

C' = C

-   -   For **table**, the function is defined by linear interpolation between values given in the attribute **tableValues** (see below). The table has *n*+1 values (that is, v<sub>0</sub> to v*<sub>n</sub>*) specifying the start and end values for *n* evenly sized interpolation regions. Interpolations use the following formula:

For a value C \< 1, find k such that k/*n* \<= C \< (k+1)/*n*

The result C' is given by C' = v<sub>k</sub> + (C - k/*n*)\**n* \* (v<sub>k+1</sub> - v<sub>k</sub>)

If C = 1 then C' = V*<sub>n</sub>*

-   -   For **discrete**, the function is defined by the step function given in the attribute **tableValues** (see below), which provides a list of *n* values (that is, v<sub>0</sub> to v<sub>n-1</sub>) in order to identify a step function consisting of n steps. The step function is defined by the following formula:

For a value C \< 1 find k such that k/*n* \<= C \< (k+1)/*n*

The result C' is given by C' = v<sub>k</sub>

If C = 1 then C' = v<sub>n-1</sub>

-   -   For **linear**, the function is defined by the following linear equation:

C' = **slope** \* C + **intercept** (see below for **slope** and **intercept**)

-   -   For **gamma**, the function is defined by the following exponential function:

C' = **amplitude** \* pow(C, **exponent**) + **offset** (see below for **amplitude**, **exponent**, and **offset**)

-   -   **tableValues**

When **type="table"**, **tableValue** is a list of numbers v<sub>0</sub>, v<sub>1</sub>, ..., v*<sub>n</sub>* separated by white space and/or a comma, which define the lookup table. An empty list results in an identity transfer function. If the attribute is not specified, then the effect is as if an empty list were provided.

-   -   **slope**

When **type="linear"**, **slope** indicates the slope of the linear function. If the attribute is not specified, then the effect is as if a value of 1 were specified.

-   -   **intercept**

When **type="linear"**, **intercept** indicates the intercept of the linear function. If the attribute is not specified, then the effect is as if a value of 0 were specified.

-   -   **amplitude**

When **type="gamma"**, **amplitude** indicates the amplitude of the gamma function. If the attribute is not specified, then the effect is as if a value of 1 were specified.

-   -   **exponent**

When **type="gamma"**, **exponent** indicates the exponent of the gamma function. If the attribute is not specified, then the effect is as if a value of 1 were specified.

-   -   **offset**

When **type="gamma"**, **offset** indicates the offset of the gamma function. If the attribute is not specified, then the effect is as if a value of 0 were specified

### Syntax

### Standards information

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.25.9

### Members

#### Properties

The **SVGFEFuncBElement** object has these properties.

-   [**amplitude**](/svg/properties/amplitude): Indicates the amplitude of the gamma function.
-   [**exponent**](/svg/properties/exponent): Indicates the exponent of the gamma function.
-   [**intercept**](/svg/properties/intercept): Indicates the intercept of the linear function.
-   [**slope**](/svg/properties/slope): Indicates the slope of the linear function.
-   [**tableValues**](/svg/properties/tableValues): Define the lookup table.
-   [**type**](/svg/properties/type_(SVGComponentTransferFunctionElement)): The type of component transfer function. The function type determines the applicability of the other attributes.

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

-   **feFuncB**

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

### Related pages (MSDN)

-   [**SVGFEComponentTransferElement**](/svg/elements/feComponentTransfer)
-   [**SVGFEFuncRElement**](/svg/elements/feFuncR)
-   [**SVGFEFuncGElement**](/svg/elements/feFuncGelement)
-   [**SVGFEFuncAElement**](/svg/elements/feFuncA)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

