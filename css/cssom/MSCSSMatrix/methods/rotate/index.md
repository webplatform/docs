---
title: rotate
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - Proprietary.
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: /css/cssom/MSCSSMatrix
    href: '/w/index.php?title=css/cssom/MSCSSMatrix/methods/rotate/css/cssom/MSCSSMatrix&action=edit&redlink=1'
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: '/w/index.php?title=css/cssom/MSCSSMatrix/methods/rotate/css/cssom/MSCSSMatrix&action=edit&redlink=1'
tags:
  - API
  - Object
  - Methods
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/cssom/MSCSSMatrix/methods/rotate/css/cssom/MSCSSMatrix
uri: css/cssom/MSCSSMatrix/methods/rotate

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [/css/cssom/MSCSSMatrix](/w/index.php?title=css/cssom/MSCSSMatrix/methods/rotate/css/cssom/MSCSSMatrix&action=edit&redlink=1)[/css/cssom/MSCSSMatrix](/w/index.php?title=css/cssom/MSCSSMatrix/methods/rotate/css/cssom/MSCSSMatrix&action=edit&redlink=1)

## <span>Syntax</span>

``` js
var object = object.rotate();
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

{

**Needs Examples**: This section should include examples.

### <span>Syntax</span>

### <span>Standards information</span>

-   [CSS Transitions Module Level 3](http://go.microsoft.com/fwlink/p/?linkid=223140), Section 10.1

### <span>Parameters</span>

*angleX* [in]
:   Type: **float**The angle (in degrees) of the rotation along the *x*-axis. If *angleY* and *angleZ* are undefined, this method becomes a rotation *angleX* degrees around the *z*-axis.
*angleY* [in, optional]
:   Type: **float**Angle (in degrees) of the rotation along the *y*-axis.
*angleZ* [in, optional]
:   Type: **float**Angle (in degrees) of the rotation along the *z*-axis.
*retMatrix* [out, retval]
:   Type: **MSCSSMatrix**The returned matrix.

## <span>See also</span>

### <span>Related articles</span>

#### <span>Transforms</span>

-   [inverse](/css/cssom/MSCSSMatrix/methods/inverse)

-   [multiply](/css/cssom/MSCSSMatrix/methods/multiply)

-   **rotate**

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

-   [translate](/css/transforms/MSCSSMatrix/translate)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### <span>Related pages (MSDN)</span>

-   `MSCSSMatrix`
