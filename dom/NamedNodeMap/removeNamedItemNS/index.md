---
title: removeNamedItemNS
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs example'
summary: 'Removes an attribute with a given name and a given namespace.'
uri: dom/NamedNodeMap/removeNamedItemNS

---
# removeNamedItemNS

## Summary

Removes an attribute with a given name and a given namespace.

*Method of [dom/NamedNodeMap](/dom/NamedNodeMap)*

## Syntax

``` {.js}
var attribute = attributes.removeNamedItemNS(/* see parameter list */);
```

## Parameters

### namespace

 Data-typeÂ
:   String

 The namespace name of the attribute to remove.

### name

 Data-typeÂ
:   String

 The local name of the desired attribute within the specified namespace.

## Return Value

Returns an object of type DOM Node.

The removed attribute node.

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NamedNodeMap](https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap) Article]

Portions of this content come from the Microsoft Developer Network: [[removeNamedItemNS](http://msdn.microsoft.com/en-us/library/ie/ff975160(v=vs.85).aspx) Article]

