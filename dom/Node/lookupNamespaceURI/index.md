---
title: 'lookupNamespaceURI'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.namespaceURI](https://developer.mozilla.org/en-US/docs/Web/API/Node.namespaceURI) Article]'
  - 'Microsoft Developer Network: [[namespaceURI Property](http://msdn.microsoft.com/en-us/library/ie/ff974771(v=vs.85).aspx) Article]'
notes:
  - 'needs example'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Node
    href: /dom/Node
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Gets the URI of the namespace associated with a namespace prefix, if any.'
tags:
  - API_Object_Methods
  - DOM
  - Needs_Examples
uri: dom/Node/lookupNamespaceURI

---
## Summary

Gets the URI of the namespace associated with a namespace prefix, if any.

Method of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

``` js
var namespaceURI = node.lookupNamespaceURI(/* see parameter list */);
```

## Parameters

### prefix

 Data-type
:   String

 The prefix, or null.

## Return Value

Returns an object of type StringString

The URI of the namespace for **prefix**. null if no namespace is found for **prefix**. The default namespace if **prefix** is null.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
