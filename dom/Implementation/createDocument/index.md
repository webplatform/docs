---
title: createDocument
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'example, compatibility'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Implementation
    href: /dom/Implementation
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Implementation
standardization_status: 'W3C Recommendation'
summary: 'Creates a Document that is not attached to a window.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Implementation/createDocument

---
## Summary

Creates a Document that is not attached to a window.

Method of [dom/Implementation](/dom/Implementation)[dom/Implementation](/dom/Implementation)

## Syntax

``` js
var newDocument = implementation.createDocument(namespace, rootElementName, doctype);
```

## Parameters

### namespace

 Data-type
:   String

 The namespace URI of the resulting document or a null value.

### rootElementName

 Data-type
:   String

 The qualified name (for example, namespace:localname) of the root element for the document or a null value.

### doctype

 Data-type
:   DOM Node

 The desired [document type](/html/elements/!DOCTYPE) for the document or a null value.

## Return Value

Returns an object of type DOM NodeDOM Node

The resulting document.

**Needs Examples**: This section should include examples.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
