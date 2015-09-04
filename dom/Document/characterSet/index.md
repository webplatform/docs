---
title: characterSet
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Last Call Working Draft'
summary: 'Gets the preferred MIME name of the document''s character encoding.'
uri: dom/Document/characterSet

---
# characterSet

## Summary

Gets the preferred MIME name of the document's character encoding.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.characterSet;
```

## Examples

``` {.js}
//displays the document's character encoding string
function showCharSet() {
    alert(document.characterSet);
}
```

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 3.1.3

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

