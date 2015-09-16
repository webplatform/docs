---
title: previousSibling
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[TreeWalker.previousSibling](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker.previousSibling) Article]'
  - 'Microsoft Developer Network: [[previousSibling Method](http://msdn.microsoft.com/en-us/library/ie/ff975265(v=vs.85).aspx) Article]'
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
summary: 'Retrieves the previous sibling of the current node in the filtered TreeWalker hierarchy and updates currentNode.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/TreeWalker/previousSibling

---
## Summary

Retrieves the previous sibling of the current node in the filtered TreeWalker hierarchy and updates currentNode.

Method of [dom/TreeWalker](/dom/TreeWalker)[dom/TreeWalker](/dom/TreeWalker)

## Syntax

``` js
var node = treewalker.previousSibling();
```

## Return Value

Returns an object of type DOM NodeDOM Node

.Object that receives the previous child of a parent node in the filtered TreeWalker hierarchy.

## Examples

``` js
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

[DOM](http://dom.spec.whatwg.org/#dom-treewalker-previoussibling)
:   Living Standard
