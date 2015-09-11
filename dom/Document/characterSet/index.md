---
title: characterSet
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
standardization_status: 'W3C Last Call Working Draft'
summary: 'Gets the preferred MIME name of the document''s character encoding.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/characterSet

---
## <span>Summary</span>

Gets the preferred MIME name of the document's character encoding.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.characterSet;
```

## <span>Examples</span>

``` js
//displays the document's character encoding string
function showCharSet() {
    alert(document.characterSet);
}
```

### <span>Syntax</span>

### <span>Standards information</span>

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 3.1.3
