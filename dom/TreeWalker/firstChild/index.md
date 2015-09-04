---
title: firstChild
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Retrieves a reference to the first child of the current node of the filtered TreeWalker hierarchy and updates currentNode.'
uri: dom/TreeWalker/firstChild

---
# firstChild

## Summary

Retrieves a reference to the first child of the current node of the filtered TreeWalker hierarchy and updates currentNode.

*Method of [dom/TreeWalker](/dom/TreeWalker)*

## Syntax

``` {.js}
var node = treewalker.firstChild(/* see parameter list */);
```

## Parameters

### oNode

 Data-typeÂ
:   any

 Object that receives the first child node in the filtered **TreeWalker** hierarchy.

## Return Value

Returns an object of type DOM Node.

Object that receives the first child node in the filtered TreeWalker hierarchy.

## Examples

``` {.js}
var treewalker = document.createTreeWalker(
    document.body,
    NodeFilter.SHOW_ELEMENT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false
);
var node = treewalker.firstChild(); // returns the first child of the root element, or null if none
```

## Notes

### Remarks

**firstChild** sets the [**currentNode**](/dom/TreeWalker/currentNode) to the returned node.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 1.2

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-treewalker-firstchild)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[TreeWalker.firstChild](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker.firstChild) Article]

Portions of this content come from the Microsoft Developer Network: [[firstChild Method](http://msdn.microsoft.com/en-us/library/ie/ff975258(v=vs.85).aspx) Article]

