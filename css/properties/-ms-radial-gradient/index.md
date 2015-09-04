---
title: -ms-radial-gradient
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Add summery, specifications, compatibility.'
uri: css/properties/-ms-radial-gradient

---
# -ms-radial-gradient

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/properties](/css/properties)</span></span>

## Syntax

``` {.js}
var result = element.-ms-radial-gradient;
element.-ms-radial-gradient = value;
```

## Examples

The following radial gradient (used as the argument for the [**background-image**](/css/properties/background-image) property) has the same three color stops as the linear gradient example . This circular gradientâ€™s line begins in the lower-left corner of the box that contains it and ends at the side of the box that is farthest from its center.

    background-image: -ms-radial-gradient(left bottom, circle farthest-side, #F7FF08 0%, #21AD11 50%, #00A3EF 80%);

    background-image: -ms-radial-gradient(left bottom, ellipse farthest-side, #F7FF08 0%, #21AD11 50%, #00A3EF 80%);

[Simply changing the shape in the previous declaration from **circle** to **ellipse** makes the gradient appear as follows: View live example]

## Notes

### Remarks

**Important**Â Â The **-ms-radial-gradient()** function has been superseded by the [**radial-gradient**](/css/radial-gradient) function, which does not require the "-ms-" prefix and has a different syntax. Though the **-ms-radial-gradient()** function is still recognized by Internet ExplorerÂ 10, Microsoft encourages you to use the [**radial-gradient**](/css/radial-gradient) function, as it is compliant with the latest version of the [CSS Image Values and Replaced Content Module Level 3 specification](http://go.microsoft.com/fwlink/p/?LinkId=252389).

### Syntax

**-ms-radial-gradient** `( <starting-point>  ,   <shape>   <size>  ,   <stop-color>   <stop-offset>  ,   <stop-color>   <stop-offset>  , ...)`

### Parameters

<dl>
<dt>
*starting-point*

</dt>
<dd>
Optional value that specifies a starting point for the gradient. This value can be one or two of the following keywords.

<dl>
<dt>
Value

</dt>
<dd>
Meaning

</dd>
<dt>
\<a id="left"/\>\<a id="LEFT"/\>

<dl>
<dt>
**left**

</dt>
</dl>
</dt>
<dd>
First value only. Indicates gradient starts from left.

</dd>
<dt>
\<a id="center"/\>\<a id="CENTER"/\>

<dl>
<dt>
**center**

</dt>
</dl>
</dt>
<dd>
First value only. Indicates gradient starts from center.

</dd>
<dt>
\<a id="right"/\>\<a id="RIGHT"/\>

<dl>
<dt>
**right**

</dt>
</dl>
</dt>
<dd>
First value only. Indicates gradient starts from right.

</dd>
<dt>
\<a id="top"/\>\<a id="TOP"/\>

<dl>
<dt>
**top**

</dt>
</dl>
</dt>
<dd>
Default. Second value only. Indicates gradient starts from top.

</dd>
<dt>
\<a id="middle"/\>\<a id="MIDDLE"/\>

<dl>
<dt>
**middle**

</dt>
</dl>
</dt>
<dd>
Second value only. Indicates gradient starts from middle

</dd>
<dt>
\<a id="bottom"/\>\<a id="BOTTOM"/\>

<dl>
<dt>
**bottom**

</dt>
</dl>
</dt>
<dd>
Second value only. Indicates gradient starts from bottom.

</dd>
</dl>
Â

</dd>
<dt>
*shape*

</dt>
<dd>
Optional value that specifies the shape of the gradient.

<dl>
<dt>
Value

</dt>
<dd>
Meaning

</dd>
<dt>
\<a id="ellipse"/\>\<a id="ELLIPSE"/\>

<dl>
<dt>
**ellipse**

</dt>
</dl>
</dt>
<dd>
Indicates gradient is in the shape of an ellipse.

</dd>
<dt>
\<a id="circle"/\>\<a id="CIRCLE"/\>

<dl>
<dt>
**circle**

</dt>
</dl>
</dt>
<dd>
Indicates gradient is in the shape of an circle.

</dd>
</dl>
Â

</dd>
<dt>
*size*

</dt>
<dd>
Optional value that specifies the size relative to the box closest to its center. Its possible values are either two space-delimited length values (or percentages) or one of the following keywords.

<dl>
<dt>
Value

</dt>
<dd>
Meaning

</dd>
<dt>
\<a id="lengths"/\>\<a id="LENGTHS"/\>

<dl>
<dt>
**lengths**

</dt>
</dl>
</dt>
<dd>
Two space-delimited length values or percentages.

</dd>
<dt>
\<a id="closest-side"/\>\<a id="CLOSEST-SIDE"/\>

<dl>
<dt>
**closest-side**

</dt>
</dl>
</dt>
<dd>
For circular gradients, this value indicates that the ending-shape is circle sized so that it exactly meets the side of the box closest to its center. For elliptical gradients, the gradient-shape is an ellipse size so that it exactly meets the vertical and horizontal sides of the box closest to its center.

</dd>
<dt>
\<a id="closest-corner"/\>\<a id="CLOSEST-CORNER"/\>

<dl>
<dt>
**closest-corner**

</dt>
</dl>
</dt>
<dd>
Sizes the gradient-shape so that it exactly meets the closest corner of the box from its center. For elliptical gradients, the gradient-shape has the same ratio of width to height that it would if **closest-side** were specified.

</dd>
<dt>
\<a id="farthest-side"/\>\<a id="FARTHEST-SIDE"/\>

<dl>
<dt>
**farthest-side**

</dt>
</dl>
</dt>
<dd>
Similar to **closest-side**, except the gradient-shape is sized to meet the side of the box that is farthest from its center (for circular gradients) or the farthest vertical and horizontal sides (for elliptical gradients).

</dd>
<dt>
\<a id="farthest-corner"/\>\<a id="FARTHEST-CORNER"/\>

<dl>
<dt>
**farthest-corner**

</dt>
</dl>
</dt>
<dd>
Sizes the gradient-shape so that it exactly meets the farthest corner of the box from its center. For elliptical gradients, the gradient-shape has the same ratio of width to height that it would if **farthest-side** were specified.

</dd>
<dt>
\<a id="contain"/\>\<a id="CONTAIN"/\>

<dl>
<dt>
**contain**

</dt>
</dl>
</dt>
<dd>
Same as **closest-side**.

</dd>
<dt>
\<a id="cover"/\>\<a id="COVER"/\>

<dl>
<dt>
**cover**

</dt>
</dl>
</dt>
<dd>
Default. Same as **farthest-corner**.

</dd>
</dl>
Â

</dd>
<dt>
*stop-color*

</dt>
<dd>
Required. Defines the color component of a stop point for the gradient. Each stop point has its own designated color, and the area between each point is filled with a continuous color transition from one to the other. This value can be any supported color value, as described in CSS Values and Units.

</dd>
<dt>
*stop-offset*

</dt>
<dd>
Optional percentage or decimal value that indicates where along the gradient line (from the center outward) to place the color stop. For instance, a value of 20% or 0.2 indicates the color stop should be placed at a point 20% of the length of the gradient line, starting from the beginning of the line.

</dd>
</dl>

## See also

### Related articles

#### Deprecated

-   **-ms-radial-gradient**

-   [-ms-repeating-linear-gradient](/css/properties/-ms-repeating-linear-gradient)

-   [-ms-repeating-radial-gradient](/css/properties/-ms-repeating-radial-gradient)

-   [MutationEvent](/dom/MutationEvent)

-   [attrChange](/dom/MutationEvent/attrChange)

-   [attrName](/dom/MutationEvent/attrName)

-   [initMutationEvent](/dom/MutationEvent/initMutationEvent)

-   [newValue](/dom/MutationEvent/newValue)

-   [prevValue](/dom/MutationEvent/prevValue)

-   [relatedNode](/dom/MutationEvent/relatedNode)

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [escape](/javascript/escape)

-   [unescape](/javascript/unescape)

#### Gradients

-   [linear-gradient](/css/functions/linear-gradient)

-   [css/functions/radial-gradient](/css/functions/radial-gradient)

-   [repeating-linear-gradient](/css/functions/repeating-linear-gradient)

-   [repeating-radial-gradient](/css/functions/repeating-radial-gradient)

-   **-ms-radial-gradient**

-   [-ms-repeating-linear-gradient](/css/properties/-ms-repeating-linear-gradient)

-   [-ms-repeating-radial-gradient](/css/properties/-ms-repeating-radial-gradient)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

