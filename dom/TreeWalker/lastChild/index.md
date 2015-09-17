---
title: 'lastChild'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[TreeWalker.lastChild](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker.lastChild) Article]'
  - 'Microsoft Developer Network: [[lastChild Method](http://msdn.microsoft.com/en-us/library/ie/ff975261(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/TreeWalker
    href: /dom/TreeWalker
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/TreeWalker
standardization_status: 'W3C Recommendation'
summary: 'Retrieves a reference to the last child of the current node of the filtered TreeWalker hierarchy and updates currentNode.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/TreeWalker/lastChild

---
## Summary

Retrieves a reference to the last child of the current node of the filtered TreeWalker hierarchy and updates currentNode.

Method of [dom/TreeWalker](/dom/TreeWalker)[dom/TreeWalker](/dom/TreeWalker)

## Syntax

``` js
var node = treewalker.lastChild();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Object that receives the last child node in the filtered TreeWalker hierarchy.

## Examples

``` js
var treewalker = document.createTreeWalker(
    document.body,
    NodeFilter.SHOW_ELEMENT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false
);
var node = treewalker.lastChild(); // returns the last visible child of the root element
```

## Notes

### Remarks

**lastChild** sets the [**currentNode**](/dom/TreeWalker/currentNode) to the returned node.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 1.2

## Related specifications

[DOM](http://dom.spec.whatwg.org/#dom-treewalker-lastchild)
:   Living Standard
