---
title: lookupNamespaceURI
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'needs example'
summary: 'Gets the URI of the namespace associated with a namespace prefix, if any.'
uri: dom/Node/lookupNamespaceURI

---
# lookupNamespaceURI

## Summary

Gets the URI of the namespace associated with a namespace prefix, if any.

*Method of [dom/Node](/dom/Node)*

## Syntax

``` {.js}
var namespaceURI = node.lookupNamespaceURI(/* see parameter list */);
```

## Parameters

### prefix

 Data-typeÂ
:   String

 The prefix, or null.

## Return Value

Returns an object of type String.

The URI of the namespace for **prefix**. null if no namespace is found for **prefix**. The default namespace if **prefix** is null.

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.namespaceURI](https://developer.mozilla.org/en-US/docs/Web/API/Node.namespaceURI) Article]

Portions of this content come from the Microsoft Developer Network: [[namespaceURI Property](http://msdn.microsoft.com/en-us/library/ie/ff974771(v=vs.85).aspx) Article]

