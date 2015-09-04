---
title: charset
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The charset attribute is used to declare the character encoding of the document.'
uri: html/attributes/charset

---
# charset

## Summary

The charset attribute is used to declare the character encoding of the document.

Applies to
:   [HTMLMetaElement](/dom/HTMLMetaElement)

The character encoding declaration must be fit within the first 1024 bytes of an HTML file, hence should be the first child in the the head element. Only one such declaration is allowed within a document.

Note that BOM and declaration in the HTTP header take precedence over in-document declaration.

It’s good practice to declare the character encoding inside the document for situations when the document will be used locally with no HTTP header involved, and as a visual cue in the source code.

## Examples

``` {.html}
<meta charset="utf-8"/>
```

## Related specifications

Specification
:   Status
[HTML Document Representation](http://www.w3.org/TR/html4/charset.html)
:   W3C Recommendation

