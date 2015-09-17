---
title: 'isSameNode'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.isSameNode](https://developer.mozilla.org/en-US/docs/Web/API/Node.isSameNode) Article]'
  - 'Microsoft Developer Network: [[isSameNode Method](http://msdn.microsoft.com/en-us/library/ie/ff975129(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Node
    href: /dom/Node
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /dom/Node
standardization_status: Deprecated
summary: 'Determines if two nodes are the same node.'
tags:
  - API_Object_Methods
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'Template:==='
    - 'Template:=='
uri: dom/Node/isSameNode

---
## Summary

Determines if two nodes are the same node.

Method of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

``` js
var isSame = node.isSameNode(/* see parameter list */);
```

## Parameters

### otherNode

 Data-type
:   DOM Node

 The node to be compared to the node that is executing the method.

## Return Value

Returns an object of type BooleanBoolean

Whether the node specified in the otherNode parameter refers to the same node.

## Examples

In the following example isSameNode is false since document.body is the body node while document.documentElement is the html node.

``` html
var isSameNode = document.body..isSameNode(document.documentElement);
```

## Usage

     This determines whether or not two references refer to the same node.  If the references refer to the same node, you can use the references interchangeably, even when using a proxy.

## Notes

Obsolete This feature is obsolete. Although it may still work in some browsers, its use is discouraged since it could be removed at any time. Try to avoid using it. In browsers where isSameNode is no longer supported // Instead of using node1.isSameNode(node2)

// use node1 [Template:===](/w/index.php?title=Template:%3D%3D%3D&action=edit&redlink=1) node2 // or node1 [Template:==](/w/index.php?title=Template:%3D%3D&action=edit&redlink=1) node2

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

[DOM Level 4 Core](http://www.w3.org/TR/domcore/)
:   Recommendation
