---
title: 'translateZ()'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: translateZ()
  topic: css
readiness: 'In Progress'
tags:
  - CSS_Functions
  - CSS
  - Needs_Summary
uri: css/functions/translateZ()

---
## Examples

The following code snippet is an example of the **translateZ** function in use. When applied to a square blue [**div**](/html/elements/div) element along with the [**perspective**](/css/functions/perspective()) function (which simulates depth), it has the effect illustrated in the image. (The light-blue square indicates the original position of the transformed element.)

``` html
div {
  transform: perspective(500px) translateZ(-60px);
}
```

### Syntax

**translateZ** `( <translation-value> )`

### Parameters

*translation-value*
:   A translation value.

### Standards information

-   [CSS Transforms Module, Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145), Section 13.2

## See also

### Related articles

#### Transforms

-   [inverse](/css/cssom/MSCSSMatrix/methods/inverse)

-   [multiply](/css/cssom/MSCSSMatrix/methods/multiply)

-   [rotate](/css/cssom/MSCSSMatrix/methods/rotate)

-   [rotate3d()](/css/functions/rotate3d())

-   [scale3d()](/css/functions/scale3d())

-   [skew()](/css/functions/skew())

-   [translate()](/css/functions/translate())

-   [translate3d()](/css/functions/translate3d())

-   [translateX()](/css/functions/translateX())

-   [translateY()](/css/functions/translateY())

-   **translateZ()**

-   [backface-visibility](/css/properties/backface-visibility)

-   [transform-origin-z](/css/properties/transform-origin-z)

-   [MSCSSMatrix](/css/transforms/MSCSSMatrix)

-   [translate](/css/transforms/MSCSSMatrix/translate)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### Related pages

-   `Transform Functions`
-   Mathematical Description of Transform Functions[Mathematical Description of Transform Functions](http://go.microsoft.com/fwlink/p/?LinkId=256246)
-   `Direct3D: Matrices`
-   Hands On: 3-D Transforms[Hands On: 3-D Transforms](http://go.microsoft.com/fwlink/?LinkId=227893)
