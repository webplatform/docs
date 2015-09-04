---
title: getAttributeNodeNS
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs example and compat tables'
summary: 'Gets an attribute node that matches the specified namespace and name.'
uri: dom/Element/getAttributeNodeNS

---
# getAttributeNodeNS

## Summary

Gets an attribute node that matches the specified namespace and name.

*Method of [dom/Element](/dom/Element)*

## Syntax

``` {.js}
var attributeNode = element.getAttributeNodeNS(namespace, name);
```

## Parameters

### namespace

 Data-typeÂ
:   String

 The namespace URI that defines the desired attribute, or a null value.

### name

 Data-typeÂ
:   Blob

 The name of the desired attribute, or a null value.

## Return Value

Returns an object of type DOM Node.

An attribute node that matches the specified namespace and attribute name, or a null value when no attribute node is found.

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

