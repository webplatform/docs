---
title: scale
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Little content; browser-specific; move/deletion candidate'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: css/cssom/MSCSSMatrix
    href: '/w/index.php?title=css/cssom/MSCSSMatrix&action=edit&redlink=1'
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: '/w/index.php?title=css/cssom/MSCSSMatrix&action=edit&redlink=1'
tags:
  - API
  - Object
  - Methods
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/cssom/MSCSSMatrix
uri: css/cssom/MSCSSMatrix/methods/scale

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [css/cssom/MSCSSMatrix](/w/index.php?title=css/cssom/MSCSSMatrix&action=edit&redlink=1)[css/cssom/MSCSSMatrix](/w/index.php?title=css/cssom/MSCSSMatrix&action=edit&redlink=1)

## Syntax

``` js
var object = object.scale();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

|Return value|Description|
|:-----------|:----------|
|S\_OK|The operation completed successfully.|

MSCSSMatrix

The returned matrix.

**Needs Examples**: This section should include examples.

### Syntax

### Standards information

-   [CSS Transitions Module Level 3](http://go.microsoft.com/fwlink/p/?linkid=223140), Section 10.1

### Parameters

*scaleX* [in]
:   Type: **float**The *x* component (in degrees) of the scale value.
*scaleY* [in, optional]
:   Type: **float**The *y* component (in degrees) of the scale value. If *scaleY* is not defined, the *y* component of the scale value is the same as the *x* component.
*scaleZ* [in, optional]
:   Type: **float**The *z* component (in degrees) of the scale value. If *scaleY* is not defined, the value of *scaleZ* is 1.
*retMatrix* [out, retval]
:   Type: **MSCSSMatrix**The returned matrix.

## See also

### Related pages (MSDN)

-   `MSCSSMatrix`
