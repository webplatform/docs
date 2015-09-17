---
title: 'namespaceURI'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.namespaceURI](https://developer.mozilla.org/en-US/docs/Web/API/Node.namespaceURI) Article]'
  - 'Microsoft Developer Network: [[namespaceURI Property](http://msdn.microsoft.com/en-us/library/ie/ff974771(v=vs.85).aspx) Article]'
notes:
  - 'needs example - awaiting upload of xml/svg samples to Renoir.'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Node
    href: /dom/Node
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the namespace URI of the fully qualified XML declaration for a node.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: dom/Node/namespaceURI

---
## Summary

Retrieves the namespace URI of the fully qualified XML declaration for a node.

Property of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

**Note**: This property is read-only.

``` js
var namespaceURI = node.namespaceURI;
```

## Return Value

Returns an object of type StringString

The namespace URI of the node, or null if there is none.

## Usage

     Enumeration of the DOM Tree. See Gecko's DOM Inspector utility.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
