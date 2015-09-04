---
title: repeating-radial-gradient
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
uri: css/functions/repeating-radial-gradient
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/functions/

---
# repeating-radial-gradient

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/functions/](/w/index.php?title=css/functions/&action=edit&redlink=1)</span></span>

## Syntax

``` {.js}
var result = element.repeating-radial-gradient;
element.repeating-radial-gradient = value;
```

## Examples

The following declaration creates a repeating circular gradient.

    background-image: repeating-radial-gradient(closest-side circle at 40px 50px, #FFF133, #16D611, #00A3EF);

    background-image: repeating-radial-gradient(closest-side at 40px 50px, #FFF133, #16D611, #00A3EF, #FFF133);

[The following declaration creates a repeating elliptical gradient. View live example]

## Notes

### Remarks

Once the last color stop has been reached, the gradient starts again at the first color stop and repeats. It's a good idea to specify identical colors for the first and last color stops to prevent abrupt color changes between each repeating group. The syntax for the **repeating-radial-gradient** function is identical to that of the [**radial-gradient**](/css/radial-gradient) function. **Important**  The Cascading Style Sheets (CSS) Gradients properties do not require a vendor prefix (that is, "-ms-") to work correctly in Internet Explorer 10. The syntax for the **repeating-radial-gradient** function given in this topic is different from that supported in previous pre-releases of Internet Explorer 10, which required the "-ms-" prefix. To maximize backward compatibility, those older implementations are still recognized, as described in [**-ms-repeating-radial-gradient**](/css/properties/-ms-repeating-radial-gradient).

### Syntax

**repeating-radial-gradient** `([ [  <shape>  ||  <size>  ] [ at  <position>  ] ? ,  | at  <position>  ,  ] ?  <color-stop>  [ ,   <color-stop>  ] +)`

### Parameters

<dl>
<dt>
*position*

</dt>
<dd>
Optional value that specifies the center of the gradient. This value can take the same values as the [**background-position**](/css/properties/background-position) property. If this value is omitted, it defaults to **center**.

</dd>
<dt>
*shape*

</dt>
<dd>
Optional value that specifies the ending shape of the gradient. If this value is omitted, the ending shape is a circle if the *size* parameter is a single length value, and an ellipse otherwise.

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
�

</dd>
<dt>
*size*

</dt>
<dd>
Optional value that specifies the size of the gradient's ending shape. If this value is omitted, it defaults to **farthest-corner**.

<dl>
<dt>
Value

</dt>
<dd>
Meaning

</dd>
<dt>
\<a id="\_length\_s\_\_"/\>\<a id="\_LENGTH\_S\_\_"/\>

<dl>
<dt>
**\<length(s)\>**

</dt>
</dl>
</dt>
<dd>
One or two space-delimited length values or two percentages. If one length value is specified, it indicates the radius of the circle. If two values (length or percent) are specified, the first value represents the horizontal radius, and the second the vertical radius. Percentage values are relative to the corresponding dimension of the gradient box. Percentages can only be used to specify the size of an elliptical gradient, not a circular one.Negative values are invalid.

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
Sizes the gradient-shape so that it exactly meets the closest corner of the box from its center. For elliptical gradients, the gradient-shape has the same ratio of width to height that it would if **closest-side** was specified.

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
Sizes the gradient-shape so that it exactly meets the farthest corner of the box from its center. For elliptical gradients, the gradient-shape has the same ratio of width to height that it would if **farthest-side** was specified.

</dd>
</dl>
�

</dd>
<dt>
*color-stop*

</dt>
<dd>
At least two color stops are required. Each color stop has one or two components—a color component and an optional position component. The first component defines the color component of a stop point for the gradient. Each stop point has its own designated color, and the area between each point is filled with a continuous color transition from one to the other. This value can be any supported color value.The second component is an optional percentage or decimal value that indicates where along the gradient ray (similar to a gradient line in a [**linear-gradient**](/css/linear-gradient), but from the center outward) to place the color stop. "0%" indicates the start of the gradient ray, and "100%" indicates the point where the gradient ray intersects the ending shape. For instance, a value of "20%" indicates the color stop should be placed at a point 20% of the length of the gradient ray, starting from the beginning of the line. Values can be negative, which indicates that the specified color for that value is at mid-transition to the next color at the center of the gradient, so the visible color at the center will be somewhere between the specified color and the next color. Values can be greater than 100%, which specifies a location a correspondingly greater distance from the center of the gradient.

</dd>
</dl>

## See also

### Related articles

#### Gradients

-   [linear-gradient](/css/functions/linear-gradient)

-   [css/functions/radial-gradient](/css/functions/radial-gradient)

-   [repeating-linear-gradient](/css/functions/repeating-linear-gradient)

-   **repeating-radial-gradient**

-   [-ms-radial-gradient](/css/properties/-ms-radial-gradient)

-   [-ms-repeating-linear-gradient](/css/properties/-ms-repeating-linear-gradient)

-   [-ms-repeating-radial-gradient](/css/properties/-ms-repeating-radial-gradient)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

