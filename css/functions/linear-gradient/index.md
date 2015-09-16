---
title: 'linear-gradient'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://jsfiddle.net/denbuzze/J2CLV/'
compatibility:
  feature: linear-gradient
  topic: css
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Defines a linear gradient as a CSS image.'
tags:
  - CSS
  - Functions
uri: css/functions/linear-gradient

---
## Summary

Defines a linear gradient as a CSS image.

## Examples

``` css
background: #1e5799;
background: -moz-linear-gradient(top, #1e5799 0%, #7db9e8 100%);
background: -webkit-gradient(linear, left top, left bottom, color-stop(0%,#1e5799), color-stop(100%,#7db9e8));
background: -webkit-linear-gradient(top, #1e5799 0%,#7db9e8 100%);
background: -o-linear-gradient(top, #1e5799 0%,#7db9e8 100%);
background: -ms-linear-gradient(top, #1e5799 0%,#7db9e8 100%);
background: linear-gradient(to bottom, #1e5799 0%,#7db9e8 100%);
filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#1e5799', endColorstr='#7db9e8',GradientType=0 );
```

[View live example](http://jsfiddle.net/denbuzze/J2CLV/)

### Syntax

**linear-gradient** `([ [  <angle>  | to  <side-or-corner>  ] , ] ?  <color-stop>  [ ,  <color-stop>  ] +)`

### Parameters

*angle*
:   Optional. The angle the gradient line should assume, expressed as a number followed by an angle units designator(for instance, "deg")."0deg" points upward and positive angles increase in a clockwise direction. Therefore, "90deg" points toward the right, "180deg" points downward, and so on.If no angle is provided, the gradient line starts in the corner or side opposite the corner or side specified by *\<side-or-corner\>*.
*side-or-corner*
:   Optional value that specifies an ending corner or side for the gradient. This value begins with "to", which is followed by one or two of the following keywords. Including one keyword specifies an ending side, and two keywords specify an ending corner.
    -   The following values can be used as the first value only:
        -   **left** Indicates gradient ends on the left.
        -   **right** Indicates gradient ends on the right.
    -   The following values can be used as the second value only:
        -   **top** Indicates gradient ends on the top.
        -   **bottom** Indicates gradient ends on the bottom.
    -   Not including any keywords or angle is equivalent to "to bottom".

*color-stop*
:   At least two color stops are required. Each color stop has one or two components—a color component and an optional position component. The first component defines the color component of a stop point for the gradient. Each stop point has its own designated color, and the area between each point is filled with a continuous color transition from one to the other. This value can be any supported color value.Each stop point can have an optional percentage or supported length value that indicates where along the gradient line to place the color stop. "0%" (or "0px", "0em", and so on) indicates the starting point (or side); "100%" indicates the ending point (or side).

## Related specifications

[CSS Image Values and Replaced Content Module Level 3](http://www.w3.org/TR/css3-images/)
:   Candidate Recommendation

## See also

### Related articles

#### Gradients

-   **linear-gradient**

-   [css/functions/radial-gradient](/css/functions/radial-gradient)

-   [repeating-linear-gradient](/css/functions/repeating-linear-gradient)

-   [repeating-radial-gradient](/css/functions/repeating-radial-gradient)

-   [-ms-radial-gradient](/css/properties/-ms-radial-gradient)

-   [-ms-repeating-linear-gradient](/css/properties/-ms-repeating-linear-gradient)

-   [-ms-repeating-radial-gradient](/css/properties/-ms-repeating-radial-gradient)
