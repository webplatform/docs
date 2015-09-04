---
title: charset
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Gets or sets the preferred MIME name of the document''s character encoding.'
uri: dom/Document/charset

---
# charset

## Summary

Gets or sets the preferred MIME name of the document's character encoding.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

``` {.js}
var result = element.charset;
element.charset = value;
```

## Examples

``` {.js}
//displays the document's character encoding string
function showCharSet() {
    alert(document.characterSet);
}

//sets the document's character encoding string
function putCharSet() {
    document.characterSet = "UTF-16";
}
```

## Usage

     On setting, if the new value is an IANA-registered alias for a character encoding supported by the user agent, the document's character encoding is set to that character encoding. Otherwise, nothing happens.

## Notes

### Remarks

For [**a**](/html/elements/a), **link**, and **script** objects, you must set the value of this property before you can retrieve it. You must set the value of this property before you can retrieve it. In Microsoft Internet Explorer 6, This property now applies to the [**a**](/html/elements/a), **link**, and **script** objects.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

