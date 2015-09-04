---
title: -ms-repeating-linear-gradient
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Add summery, specifications, compatibility.'
uri: css/properties/-ms-repeating-linear-gradient

---
# -ms-repeating-linear-gradient

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/properties](/css/properties)</span></span>

## Syntax

``` {.js}
var result = element.-ms-repeating-linear-gradient;
element.-ms-repeating-linear-gradient = value;
```

## Examples

The following declaration creates a repeating linear gradient.

    background-image: -ms-repeating-linear-gradient(top right, #FFF133 0%, #16D611 50%, #00A3EF 80%);

## Notes

### Remarks

**Important**  The **-ms-repeating-linear-gradient()** function has been superseded by the [**repeating-linear-gradient**](/css/repeating-linear-gradient) function, which does not require the "-ms-" prefix and has a different syntax. Though the **-ms-repeating-linear-gradient()** function is still recognized by Internet Explorer 10, Microsoft encourages you to use the [**repeating-linear-gradient**](/css/repeating-linear-gradient) function, as it is compliant with the latest version of the [CSS Image Values and Replaced Content Module Level 3 specification](http://go.microsoft.com/fwlink/p/?LinkId=252389). Once the last stop point has been reached, the gradient transitions to the first stop point and repeats. The syntax for the **-ms-repeating-linear-gradient()** function is identical to that of the [**-ms-linear-gradient()**](/css/properties/-ms-linear-gradient) function.

### Syntax

**-ms-repeating-linear-gradient** `( <angle>   <starting-point>  ,   <stop-color>   <stop-offset>  ,   <stop-color>   <stop-offset>  , ...)`

### Parameters

<dl>
<dt>
*angle*

</dt>
<dd>
Optional. The angle the gradient-line should assume, expressed as a number followed by an angle units designator(`deg`, `grad`, `rad`, or `turn`).For more information about supported angle units,see CSS Values and Units.For instance, 0deg points upwards, 90deg points toward the right, and positive angles go clockwise. If no angle is provided, the gradient line starts in the corner or side specified by *\<starting-point\>* and ends in the opposite corner or side.

</dd>
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
�

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
Optional percentage or decimal value that indicates where along the gradient line to place the color stop.

</dd>
</dl>

## See also

### Related articles

#### Deprecated

-   [-ms-radial-gradient](/css/properties/-ms-radial-gradient)

-   **-ms-repeating-linear-gradient**

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

-   [-ms-radial-gradient](/css/properties/-ms-radial-gradient)

-   **-ms-repeating-linear-gradient**

-   [-ms-repeating-radial-gradient](/css/properties/-ms-repeating-radial-gradient)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

