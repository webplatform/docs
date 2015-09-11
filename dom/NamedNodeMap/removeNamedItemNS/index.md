---
title: removeNamedItemNS
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NamedNodeMap](https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap) Article]'
  - 'Microsoft Developer Network: [[removeNamedItemNS](http://msdn.microsoft.com/en-us/library/ie/ff975160(v=vs.85).aspx) Article]'
notes:
  - 'Needs example'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/NamedNodeMap
    href: /dom/NamedNodeMap
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/NamedNodeMap
standardization_status: 'W3C Recommendation'
summary: 'Removes an attribute with a given name and a given namespace.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/NamedNodeMap/removeNamedItemNS

---
## <span>Summary</span>

Removes an attribute with a given name and a given namespace.

Method of [dom/NamedNodeMap](/dom/NamedNodeMap)[dom/NamedNodeMap](/dom/NamedNodeMap)

## <span>Syntax</span>

``` js
var attribute = attributes.removeNamedItemNS(/* see parameter list */);
```

## <span>Parameters</span>

### <span>namespace</span>

 Data-type
:   String

 The namespace name of the attribute to remove.

### <span>name</span>

 Data-type
:   String

 The local name of the desired attribute within the specified namespace.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The removed attribute node.

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
