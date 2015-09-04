---
title: previousSibling
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the previous sibling of the current node in the filtered TreeWalker hierarchy and updates currentNode.'
uri: dom/TreeWalker/previousSibling

---
# previousSibling

## Summary

Retrieves the previous sibling of the current node in the filtered TreeWalker hierarchy and updates currentNode.

*Method of [dom/TreeWalker](/dom/TreeWalker)*

## Syntax

``` {.js}
var node = treewalker.previousSibling();
```

## Return Value

Returns an object of type DOM Node.

.Object that receives the previous child of a parent node in the filtered TreeWalker hierarchy.

## Examples

``` {.js}
var treewalker = document.createTreeWalker(
    document.body,
    NodeFilter.SHOW_ELEMENT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false
);
var node = treewalker.previousSibling(); // returns null as there is no previous sibiling
```

## Notes

### Remarks

**previousSibling** sets the [**currentNode**](/dom/TreeWalker/currentNode) to the returned node. It returns null if there are no more child nodes.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 1.2

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-treewalker-previoussibling)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[TreeWalker.previousSibling](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker.previousSibling) Article]

Portions of this content come from the Microsoft Developer Network: [[previousSibling Method](http://msdn.microsoft.com/en-us/library/ie/ff975265(v=vs.85).aspx) Article]

