---
title: translate()
tags:
  - CSS
  - Functions
readiness: 'Ready to Use'
summary: 'Transform function for a 2d translation which sets the position of an element to a new one, described by two vectors (x, y). The y value is optional.'
code_samples:
  - 'http://codepen.io/Fischaela/pen/Lqmxb'
uri: css/functions/translate()

---
# translate()

## Summary

Transform function for a 2d translation which sets the position of an element to a new one, described by two vectors (x, y). The y value is optional.

## Syntax

-   **translate ( \<translation-value-x\> )**
-   **translate ( \<translation-value-x\>, \<translate-value-y\> )**

## Parameters

**translation-value-x**

*Value for the translation across the x-axis. Can be a [length](/css/data_types/length) value or a [percentage](/css/data_types/percentage) value. Value for the y-axis translation is assumed to be zero.*

**translation-value-x, translate-value-y**

*First value describes the translation across the x-axis, the second across the y-axis. Values can be a [length](/css/data_types/length) or a [percentage](/css/data_types/percentage) value.*

## Examples

The example shows three div elements, that are transformed individually with the translate() function.

1.  The translation of element-1 visually is making no difference from its origin, because it has twice **zero** as translation-values.
2.  The second translation only provides a **single translation-value-x**, the second value is set to zero by default here. The div moves 20px to the right.
3.  For element-3 **both translation-values** are set. The div is moved 40px to the right and 80px down.

``` {.css}
.element-1 {
    transform: translate(0, 0);
}

.element-2 {
    transform: translate(20px);
}

.element-3 {
    transform: translate(40px, 80px);
}
```

[View live example](http://codepen.io/Fischaela/pen/Lqmxb)

## See also

### Related articles

#### Transforms

-   [inverse](/css/cssom/MSCSSMatrix/methods/inverse)

-   [multiply](/css/cssom/MSCSSMatrix/methods/multiply)

-   [rotate](/css/cssom/MSCSSMatrix/methods/rotate)

-   [rotate3d()](/css/functions/rotate3d())

-   [scale3d()](/css/functions/scale3d())

-   [skew()](/css/functions/skew())

-   **translate()**

-   [translate3d()](/css/functions/translate3d())

-   [translateX()](/css/functions/translateX())

-   [translateY()](/css/functions/translateY())

-   [translateZ()](/css/functions/translateZ())

-   [backface-visibility](/css/properties/backface-visibility)

-   [transform-origin-z](/css/properties/transform-origin-z)

-   [MSCSSMatrix](/css/transforms/MSCSSMatrix)

-   [translate](/css/transforms/MSCSSMatrix/translate)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### External resources

-   [CSS Transforms Module, Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145), Section 13.1
-   [Mathematical Description of Transform Functions](http://go.microsoft.com/fwlink/p/?LinkId=256246)
-   [Hands On: 2D Transforms](http://go.microsoft.com/fwlink/?LinkID=240163)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

