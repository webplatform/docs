---
title: scale3d()
tags:
  - CSS
  - Functions
readiness: 'Ready to Use'
notes:
  - 'Could benefit from demonstrative images.'
summary: 'Defines a three-dimensional transformation to change the scale of the element by setting specific scaling factors in each of the x, y, and z directions.  All three parameters must be specified.'
code_samples:
  - 'http://gist.github.com/5305309'
uri: css/functions/scale3d()

---
# scale3d()

## Summary

Defines a three-dimensional transformation to change the scale of the element by setting specific scaling factors in each of the x, y, and z directions. All three parameters must be specified.

## Examples

The following code snippet is an example of the **scale3d** function in use. When applied to a square blue [**div**](/html/elements/div) element, it has the effect illustrated in the image. (The light-blue square indicates the original position of the transformed element.)

``` {.css}
div {
  transform: scale3d(0.5, -0.5, 1.5);
}
```

[View live example](http://code.webplatform.org/gist/5305309)

### Syntax

**scale3d** `( <scaling-value-x>  ,  <scaling-value-y>  ,  <scaling-value-z> )`

### Parameters

*scaling-value-x*
:   Numerical value by which to scale the specified element in the *x*-direction.
*scaling-value-y*
:   Numerical value by which to scale the specified element in the *y*-direction.
*scaling-value-z*
:   Numerical value by which to scale the specified element in the *z*-direction.

### Standards information

-   [CSS Transforms Module, Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145), Section 13.2

## See also

### Related articles

#### Transforms

-   [inverse](/css/cssom/MSCSSMatrix/methods/inverse)

-   [multiply](/css/cssom/MSCSSMatrix/methods/multiply)

-   [rotate](/css/cssom/MSCSSMatrix/methods/rotate)

-   [rotate3d()](/css/functions/rotate3d())

-   **scale3d()**

-   [skew()](/css/functions/skew())

-   [translate()](/css/functions/translate())

-   [translate3d()](/css/functions/translate3d())

-   [translateX()](/css/functions/translateX())

-   [translateY()](/css/functions/translateY())

-   [translateZ()](/css/functions/translateZ())

-   [backface-visibility](/css/properties/backface-visibility)

-   [transform-origin-z](/css/properties/transform-origin-z)

-   [MSCSSMatrix](/css/transforms/MSCSSMatrix)

-   [translate](/css/transforms/MSCSSMatrix/translate)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### Related pages (MSDN)

-   `Transform Functions`
-   `Mathematical Description of Transform Functions`
-   `Direct3D: Matrices`
-   `Hands On: 3-D Transforms`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

