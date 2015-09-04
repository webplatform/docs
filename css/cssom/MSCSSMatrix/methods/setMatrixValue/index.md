---
title: setMatrixValue
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Not Ready'
notes:
  - 'Little content; browser-specific; move/deletion candidate'
uri: css/cssom/MSCSSMatrix/methods/setMatrixValue
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/cssom/MSCSSMatrix

---
# setMatrixValue

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [css/cssom/MSCSSMatrix](/w/index.php?title=css/cssom/MSCSSMatrix&action=edit&redlink=1)*

## Syntax

``` {.js}
var object = object.setMatrixValue();
```

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

<dl data-table="wikitable">
<dt>
Return code/value

</dt>
<dd>
Description

</dd>
<dt>
S\_OK

</dt>
<dd>
The operation completed successfully.

</dd>
<dt>
DOMException.SYNTAX\_ERR

12

</dt>
<dd>
The transformValue string cannot be parsed into an MSCSSMatrix. This occurs when the string is not a valid value for the transform property, or if the string contains relative units.

</dd>
</dl>
Â

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Using the **setMatrixValue** method and setting the [**MSCSSMatrix**](/css/transforms/MSCSSMatrix) attributes individually are the only ways to modify the current matrix. No other method will alter the current matrix.

### Syntax

### Standards information

-   [CSS Transitions Module Level 3](http://go.microsoft.com/fwlink/p/?linkid=223140), Section 10.1

### Parameters

*transformValue* [in]
:   Type: **DOMString**A string in the form of an acceptable value for the [**transform**](/css/transforms/transform) property in CSS.

## See also

### Related pages (MSDN)

-   `MSCSSMatrix`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

