---
title: toString
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Not Ready'
notes:
  - 'Little content; browser-specific; move/deletion candidate'
uri: css/cssom/MSCSSMatrix/methods/toString
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/cssom/MSCSSMatrix
    - css/MSCSSMatrix/apis/properties/a

---
# toString

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [css/cssom/MSCSSMatrix](/w/index.php?title=css/cssom/MSCSSMatrix&action=edit&redlink=1)*

## Syntax

``` {.js}
var object = object.toString();
```

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

Return value
:   Description
S\_OK
:   The operation completed successfully.

Â

DOMString

A string value that corresponds to the matrix. This string value contains matrix(, followed by a comma-and-whitespace-delimited list of matrix values, followed by ).

For a 2-D transform matrix, the matrix value list is ordered [**a**](/w/index.php?title=css/MSCSSMatrix/apis/properties/a&action=edit&redlink=1), [**b**](/css/cssom/MSCSSMatrix/properties/b), [**c**](/css/cssom/MSCSSMatrix/properties/c), [**d**](/css/cssom/MSCSSMatrix/properties/d), [**e**](/css/cssom/MSCSSMatrix/properties/e), [**f**](/css/cssom/MSCSSMatrix/properties/f).

For a 3-D transform matrix, the matrix value list is ordered [**m11**](/css/cssom/MSCSSMatrix/properties/m11), [**m21**](/css/cssom/MSCSSMatrix/properties/m21), [**m31**](/css/cssom/MSCSSMatrix/properties/m31), [**m41**](/css/cssom/MSCSSMatrix/properties/m41), [**m12**](/css/cssom/MSCSSMatrix/properties/m12), [**m22**](/css/cssom/MSCSSMatrix/properties/m22), [**m32**](/css/cssom/MSCSSMatrix/properties/m32), [**m42**](/css/cssom/MSCSSMatrix/properties/m42), [**m13**](/css/cssom/MSCSSMatrix/properties/m13), [**m23**](/css/cssom/MSCSSMatrix/properties/m23), [**m33**](/css/cssom/MSCSSMatrix/properties/m33), [**m43**](/css/cssom/MSCSSMatrix/properties/m43), [**m14**](/css/cssom/MSCSSMatrix/properties/m14), [**m24**](/css/cssom/MSCSSMatrix/properties/m24), [**m34**](/css/cssom/MSCSSMatrix/properties/m34), [**m44**](/css/cssom/MSCSSMatrix/properties/m44).

**Needs Examples**: This section should include examples.

### Syntax

### Standards information

-   [CSS Transitions Module Level 3](http://go.microsoft.com/fwlink/p/?linkid=223140), Section 10.1

### Parameters

<dl>
<dt>
*matrixString* [out, retval]

</dt>
<dd>
Type: **DOMString**A string value that corresponds to the matrix. This string value contains `matrix(`, followed by a comma-and-whitespace-delimited list of matrix values, followed by `)`.

<dl>
<dt>
Value

</dt>
<dd>
Meaning

</dd>
<dt>
\<a id="matrix\_a\_\_b\_\_c\_\_d\_\_e\_\_f\_"/\>\<a id="MATRIX\_A\_\_B\_\_C\_\_D\_\_E\_\_F\_"/\>

<dl>
<dt>
**matrix(a, b, c, d, e, f)**

</dt>
</dl>
</dt>
<dd>
For a 2-D transform matrix, the matrix value list is ordered [**a**](/w/index.php?title=css/MSCSSMatrix/apis/properties/a&action=edit&redlink=1), [**b**](/css/cssom/MSCSSMatrix/properties/b), [**c**](/css/cssom/MSCSSMatrix/properties/c), [**d**](/css/cssom/MSCSSMatrix/properties/d), [**e**](/css/cssom/MSCSSMatrix/properties/e), [**f**](/css/cssom/MSCSSMatrix/properties/f).

</dd>
<dt>
\<a id="matrix\_m11\_\_m21\_\_m31\_\_m41\_\_m12\_\_m22\_\_m32\_\_m42\_\_m13\_\_m23\_\_m33\_\_m43\_\_m14\_\_m24\_\_m34\_\_m44\_"/\>\<a id="MATRIX\_M11\_\_M21\_\_M31\_\_M41\_\_M12\_\_M22\_\_M32\_\_M42\_\_M13\_\_M23\_\_M33\_\_M43\_\_M14\_\_M24\_\_M34\_\_M44\_"/\>

<dl>
<dt>
**matrix(m11, m21, m31, m41, m12, m22, m32, m42, m13, m23, m33, m43, m14, m24, m34, m44)**

</dt>
</dl>
</dt>
<dd>
For a 3-D transform matrix, the matrix value list is ordered [**m11**](/css/cssom/MSCSSMatrix/properties/m11), [**m21**](/css/cssom/MSCSSMatrix/properties/m21), [**m31**](/css/cssom/MSCSSMatrix/properties/m31), [**m41**](/css/cssom/MSCSSMatrix/properties/m41), [**m12**](/css/cssom/MSCSSMatrix/properties/m12), [**m22**](/css/cssom/MSCSSMatrix/properties/m22), [**m32**](/css/cssom/MSCSSMatrix/properties/m32), [**m42**](/css/cssom/MSCSSMatrix/properties/m42), [**m13**](/css/cssom/MSCSSMatrix/properties/m13), [**m23**](/css/cssom/MSCSSMatrix/properties/m23), [**m33**](/css/cssom/MSCSSMatrix/properties/m33), [**m43**](/css/cssom/MSCSSMatrix/properties/m43), [**m14**](/css/cssom/MSCSSMatrix/properties/m14), [**m24**](/css/cssom/MSCSSMatrix/properties/m24), [**m34**](/css/cssom/MSCSSMatrix/properties/m34), [**m44**](/css/cssom/MSCSSMatrix/properties/m44).

</dd>
</dl>
Â

</dd>
</dl>

## See also

### Related pages (MSDN)

-   `MSCSSMatrix`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

