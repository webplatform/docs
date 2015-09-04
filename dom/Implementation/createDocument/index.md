---
title: createDocument
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'example, compatibility'
summary: 'Creates a Document that is not attached to a window.'
uri: dom/Implementation/createDocument

---
# createDocument

## Summary

Creates a Document that is not attached to a window.

*Method of [dom/Implementation](/dom/Implementation)*

## Syntax

``` {.js}
var newDocument = implementation.createDocument(namespace, rootElementName, doctype);
```

## Parameters

### namespace

 Data-typeÂ
:   String

 The namespace URI of the resulting document or a null value.

### rootElementName

 Data-typeÂ
:   String

 The qualified name (for example, namespace:localname) of the root element for the document or a null value.

### doctype

 Data-typeÂ
:   DOM Node

 The desired [document type](/html/elements/!DOCTYPE) for the document or a null value.

## Return Value

Returns an object of type DOM Node.

The resulting document.

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

