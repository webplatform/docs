---
title: 'skew()'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5305245'
compatibility:
  feature: skew()
  topic: css
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: 'Defines a two-dimensional transformation consisting of simultaneous skew transformations of the X and Y axes.  Not recommended and supported only for backwards compatibility; use a combination of skewX(angle), skewY(angle) and/or rotate(angle) instead.'
tags:
  - CSS
  - Functions
uri: css/functions/skew()

---
## Summary

Defines a two-dimensional transformation consisting of simultaneous skew transformations of the X and Y axes. Not recommended and supported only for backwards compatibility; use a combination of skewX(angle), skewY(angle) and/or rotate(angle) instead.

## Examples

The following code snippet is an example of the **skew** function in use. When applied to a square blue [**div**](/html/elements/div) element, it has the effect illustrated in the image. (The light-blue square indicates the original position of the transformed element.)

``` css
div {
  transform: skew(42deg, -12deg);
}
```

[View live example](http://code.webplatform.org/gist/5305245)

### Syntax

**skew** `( <angle-x>  ,  <angle-y> )`

### Parameters

*angle-x*
:   The angle by which the element is skewed along the *x*-axis. This value is expressed as a number followed by a supported angle unit.
*angle-y*
:   The angle by which the element is skewed along the *y*-axis. This value is expressed as a number followed by a supported angle unit.

## See also

### Related articles

#### Transforms

-   [inverse](/css/cssom/MSCSSMatrix/methods/inverse)

-   [multiply](/css/cssom/MSCSSMatrix/methods/multiply)

-   [rotate](/css/cssom/MSCSSMatrix/methods/rotate)

-   [rotate3d()](/css/functions/rotate3d())

-   [scale3d()](/css/functions/scale3d())

-   **skew()**

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

### Related pages

-   `Transform Functions`
-   Mathematical Description of Transform Functions[Mathematical Description of Transform Functions](http://go.microsoft.com/fwlink/p/?LinkId=256246)
-   Hands On: 2D Transforms[Hands On: 2D Transforms](http://go.microsoft.com/fwlink/?LinkID=240163)
