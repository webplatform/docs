---
title: rotateAxisAngle
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Not Ready'
notes:
  - 'Little content; browser-specific; move/deletion candidate'
uri: css/cssom/MSCSSMatrix/methods/rotateAxisAngle
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/cssom/MSCSSMatrix

---
# rotateAxisAngle

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [css/cssom/MSCSSMatrix](/w/index.php?title=css/cssom/MSCSSMatrix&action=edit&redlink=1)*

## Syntax

``` {.js}
var object = object.rotateAxisAngle();
```

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

Return value
:   Description
S\_OK
:   The operation completed successfully.

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

### Related pages (MSDN)

-   `MSCSSMatrix`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

