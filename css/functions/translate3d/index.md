---
title: 'translate3d()'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: translate3d()
  topic: css
notes:
  - 'might be able to merge with regular translate function, with a notation on how the 3D version differs'
readiness: 'Ready to Use'
summary: 'Transform function for a 3d translation which moves an element on x-axis, y-axis and z-axis by the given values.'
tags:
  - CSS_Functions
  - CSS
uri: css/functions/translate3d()

---
## Summary

Transform function for a 3d translation which moves an element on x-axis, y-axis and z-axis by the given values.

## Syntax

**translate3d ( \<translation-value-x\>, \<translation-value-y\>, \<translation-value-z\> )**

## Parameters

**translation-value-x, translation-value-y, translation-value-z**

*translation-value-x and translation-value-y represent vector values x and y and can be a [length](/css/data_types/length) or a [percentage](/css/data_types/percentage) value.*

*translation-value-z is the third vector value and defines the translation in the direction of the z-axis (3rd dimension).* **Attention:** *It can only be a [length](/css/data_types/length) value, percentage is not supported.*

## Examples

The example shows three div elements, that are transformed individually with the translateY() function.

1.  The translation of the first element moves it 150 pixels to the right along the x-axis.
2.  The second element is moved 120 pixels down along the positive direction of the y-axis.
3.  The last translation of element-3 is moving the div 120 pixels in the negative direction of the z-axis. Note that you have to apply a value for the [perspective](/css/properties/perspective) also, since without it the translation is not visible.

``` css
.element-1 {
    transform: translate3d(150px, 0, 0);
}

.element-2 {
    transform: translate3d(0, 120px, 0);
}

.element-3 {
    transform: perspective(400) translate3d(0, 0, -120px);
}
```

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

-   **translate3d()**

-   [translateX()](/css/functions/translateX())

-   [translateY()](/css/functions/translateY())

-   [translateZ()](/css/functions/translateZ())

-   [backface-visibility](/css/properties/backface-visibility)

-   [transform-origin-z](/css/properties/transform-origin-z)

-   [MSCSSMatrix](/css/transforms/MSCSSMatrix)

-   [translate](/css/transforms/MSCSSMatrix/translate)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### External resources

-   [CSS Transforms Module, Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145), Section 13.2
-   [Mathematical Description of Transform Functions](http://go.microsoft.com/fwlink/p/?LinkId=256246)
-   [Hands On: 3-D Transforms](http://go.microsoft.com/fwlink/?LinkId=227893)
