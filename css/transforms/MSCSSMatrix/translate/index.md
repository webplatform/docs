---
title: translate
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs title, description, example, fix table coding in Parameters'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: css/transforms/MSCSSMatrix
    href: /css/transforms/MSCSSMatrix
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /css/transforms/MSCSSMatrix
tags:
  - API
  - Object
  - Methods
  - DOM
uri: css/transforms/MSCSSMatrix/translate

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [css/transforms/MSCSSMatrix](/css/transforms/MSCSSMatrix)[css/transforms/MSCSSMatrix](/css/transforms/MSCSSMatrix)

## Syntax

``` js
var object = object.translate();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

{

**Needs Examples**: This section should include examples.

### Syntax

### Standards information

-   [CSS Transitions Module Level 3](http://go.microsoft.com/fwlink/p/?linkid=223140), Section 10.1

### Parameters

*offsetX* [in]
:   Type: **float**The translation offset along the *x*-axis.
*offsetY* [in]
:   Type: **float**The translation offset along the *y*-axis.
*offsetZ* [in, optional]
:   Type: **float**The translation offset along the *z*-axis.
*retMatrix* [out, retval]
:   Type: **MSCSSMatrix**The returned matrix.

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

-   [translateZ()](/css/functions/translateZ())

-   [backface-visibility](/css/properties/backface-visibility)

-   [transform-origin-z](/css/properties/transform-origin-z)

-   [MSCSSMatrix](/css/transforms/MSCSSMatrix)

-   **translate**

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### Related pages (MSDN)

-   `MSCSSMatrix`
