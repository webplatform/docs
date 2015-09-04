---
title: background-repeat
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Background-repeat defines if and how background images will be repeated after they have been sized and positioned'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background-repeat.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/backgroundRepeat.htm'
uri: css/properties/background-repeat

---
# background-repeat

## Summary

Background-repeat defines if and how background images will be repeated after they have been sized and positioned

## Overview table

[Initial value](/css/concepts/initial_value)
:   `repeat`
Applies to
:   All elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   A list, each item consisting of two keywords, one per dimension
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   `backgroundRepeat`
Percentages
:   N/A

## Syntax

-   `background-repeat: <repeat-style>`

## Values

\<repeat-style\>
:   Keyword(s) indicating the repeat pattern.

`repeat`
:   Default. In CSS2.1, the image is repeated horizontally and vertically. In CSS3, if two keywords are used, the image is repeated along the relevant axis.
`no-repeat`
:   The image is not repeated.
`repeat-x`
:   The image is repeated along the horizontal axis.
`repeat-y`
:   The image is repeated along the vertical axis.
`round`
:   The image is repeated as often as will fit into the background area, and is rescaled if necessary to make it fit a whole number of times. **(CSS3)**
`space`
:   The image is repeated as often as will fit into the background area a whole number of times, and is spaced out so that the first and last ones touch the edges. **(CSS3)**

## Examples

The following examples use the **background-repeat** attribute and the **background-repeat** property to specify whether the background image is tiled.

This example uses a call to an embedded (global) style sheet to tile the image.

``` {.css}
<STYLE>
    .style1 { background-image:url(sphere.jpg);
        background-repeat:repeat }
    .style2 { background-image:url(sphere.jpeg);
        background-repeat:no-repeat }
</STYLE>
</HEAD>
<BODY>
<SPAN onmouseover="this.className='style1'"
onmouseout="this.className='style2'" onclick="this.className=">
. . . </SPAN>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background-repeat.htm)

This example shows how to use inline scripting to tile the image.

``` {.css}
<SPAN onmouseover="this.style.backgroundImage='url(sphere.jpeg)';
this.style.backgroundRepeat='repeat'">
:
</SPAN>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/backgroundRepeat.htm)

## Usage

     In CSS2.1, only one keyword is permitted, affecting both the horizontal and vertical axes.

In CSS3, one or two keywords are permitted. One keyword affects both axes in the same way as CSS2.1 If two keywords are used, the first applies to the horizontal axis, and the second to the vertical axis.

If an element has multiple background images, the repeat pattern for each image can be set by assigning a comma-separated list of individual values. The values are applied to the background images in the same order as they are listed in the `background-image` property.

## Related specifications

Specification
:   Status
[CSS Level 3](http://www.w3.org/TR/css3-background/)
:   Candidate Recommendation
[CSS Level 2 (revision 1)](http://www.w3.org/TR/CSS21/colors.html#propdef-background)
:   Recommendation
[CSS Level 1](http://www.w3.org/TR/REC-CSS1/#color-and-background-properties)
:   Recommendation

## See also

### Related articles

#### Background

-   [background](/css/cssom/properties/background)

-   [background](/css/properties/background)

-   [background-attachment](/css/properties/background-attachment)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-clip](/css/properties/background-clip)

-   [background-color](/css/properties/background-color)

-   [background-image](/css/properties/background-image)

-   [background-origin](/css/properties/background-origin)

-   [background-position](/css/properties/background-position)

-   [background-position-x](/css/properties/background-position-x)

-   [background-position-y](/css/properties/background-position-y)

-   **background-repeat**

-   [background-size](/css/properties/background-size)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/).

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

