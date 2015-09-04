---
title: lastChild
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Retrieves a reference to the last child of the current node of the filtered TreeWalker hierarchy and updates currentNode.'
uri: dom/TreeWalker/lastChild

---
# lastChild

## Summary

Retrieves a reference to the last child of the current node of the filtered TreeWalker hierarchy and updates currentNode.

*Method of [dom/TreeWalker](/dom/TreeWalker)*

## Syntax

``` {.js}
var node = treewalker.lastChild();
```

## Return Value

Returns an object of type DOM Node.

Object that receives the last child node in the filtered TreeWalker hierarchy.

## Examples

``` {.js}
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

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-treewalker-lastchild)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[TreeWalker.lastChild](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker.lastChild) Article]

Portions of this content come from the Microsoft Developer Network: [[lastChild Method](http://msdn.microsoft.com/en-us/library/ie/ff975261(v=vs.85).aspx) Article]

