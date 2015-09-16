---
title: 'createDocumentType'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, compatibility, more description'
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
summary: 'Creates a Document Type node.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Implementation/createDocumentType

---
## Summary

Creates a Document Type node.

Method of [dom/Implementation](/dom/Implementation)[dom/Implementation](/dom/Implementation)

## Syntax

``` js
var object = implementation.createDocumentType(qualifiedName, publicID, systemId);
```

## Parameters

### qualifiedName

 Data-type
:   String

 The name of the [document type](/html/elements/!DOCTYPE). When you use XML namespaces, this name can be a qualified name (for example, namespace:localname).

### publicID

 Data-type
:   String

 The public identifier of the [document type](/html/elements/!DOCTYPE) or null.

### systemId

 Data-type
:   String

 The system identifier of the [document type](/html/elements/!DOCTYPE) or null.

## Return Value

Returns an object of type DOM NodeDOM Node

The created [document type](/html/elements/!DOCTYPE) object.

**Needs Examples**: This section should include examples.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
