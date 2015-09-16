---
title: rotateAxisAngle
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
uri: css/cssom/MSCSSMatrix/methods/rotateAxisAngle

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [css/cssom/MSCSSMatrix](/w/index.php?title=css/cssom/MSCSSMatrix&action=edit&redlink=1)[css/cssom/MSCSSMatrix](/w/index.php?title=css/cssom/MSCSSMatrix&action=edit&redlink=1)

## Syntax

``` js
var object = object.rotateAxisAngle();
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

*x* [in]
:   Type: **float**The *x* component of the axis vector.
*y* [in]
:   Type: **float**The *y* component of the axis vector.
*z* [in]
:   Type: **float**The *z* component of the axis vector.
*angle* [in]
:   Type: **float**The angle (in degrees) of the rotation about the axis vector.
*retMatrix* [out, retval]
:   Type: **MSCSSMatrix**The returned matrix.

## See also

### Related pages

-   `MSCSSMatrix`
