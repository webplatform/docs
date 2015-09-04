---
title: translateY()
tags:
  - CSS
  - Functions
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Transform function for a 2d translation which moves an element on the y-axis by the given value. Note that the y-axis increases vertically downwards: positive lengths shift the element down, while negative lengths shift it up.'
code_samples:
  - 'http://codepen.io/Fischaela/pen/uxgil'
uri: css/functions/translateY()

---
# translateY()

## Summary

Transform function for a 2d translation which moves an element on the y-axis by the given value. Note that the y-axis increases vertically downwards: positive lengths shift the element down, while negative lengths shift it up.

## Syntax

**translateY( \<translation-value\> )**

## Parameters

**translation-value**

*Value for the translation across the y-axis. Can be a [length](/css/data_types/length) or a [percentage](/css/data_types/percentage) value.*

## Examples

The example shows three div elements, that are transformed individually with the translateY() function.

1.  The translation of the first element moves it 10 pixels up along the y-axis.
2.  You can also provide a negative value. In this case, element-2 is moved 20 pixels to the top, in the negative direction on the y-axis.
3.  Using a percentage value of 50 percent moves element-3 in positive y-direction by a value which matches 50 percent of the element-3's width. In this case element-3 has a 100 pixel width, so it is moved 50 pixels up.

``` {.css}
.element-1 {
    transform: translateY(10px);
}

.element-2 {
    transform: translateY(-20px);
}

.element-3 {
    transform: translateY(50%);
}
```

[View live example](http://codepen.io/Fischaela/pen/uxgil)

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

-   **translateY()**

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

