---
title: createDocumentType
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'examples, compatibility, more description'
summary: 'Creates a Document Type node.'
uri: dom/Implementation/createDocumentType

---
# createDocumentType

## Summary

Creates a Document Type node.

*Method of [dom/Implementation](/dom/Implementation)*

## Syntax

``` {.js}
var object = implementation.createDocumentType(qualifiedName, publicID, systemId);
```

## Parameters

### qualifiedName

 Data-typeÂ
:   String

 The name of the [document type](/html/elements/!DOCTYPE). When you use XML namespaces, this name can be a qualified name (for example, namespace:localname).

### publicID

 Data-typeÂ
:   String

 The public identifier of the [document type](/html/elements/!DOCTYPE) or null.

### systemId

 Data-typeÂ
:   String

 The system identifier of the [document type](/html/elements/!DOCTYPE) or null.

## Return Value

Returns an object of type DOM Node.

The created [document type](/html/elements/!DOCTYPE) object.

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

