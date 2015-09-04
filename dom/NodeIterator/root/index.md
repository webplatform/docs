---
title: root
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The NodeIterator.root read-only property represents the Node that is the root of what the NodeIterator traverses.'
uri: dom/NodeIterator/root

---
# root

## Summary

The NodeIterator.root read-only property represents the Node that is the root of what the NodeIterator traverses.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/NodeIterator](/dom/NodeIterator)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var node = element.root;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

## Examples

``` {.js}
var nodeIterator = document.createNodeIterator(
    document.body,
    NodeFilter.SHOW_ELEMENT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false
);
root = nodeIterator.root; // document.body in this case
```

### Syntax

root = nodeIterator.root;

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 1.2

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-nodeiterator-root)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NodeIterator.root](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.root) Article]

Portions of this content come from the Microsoft Developer Network: [[root Property](http://msdn.microsoft.com/en-us/library/ie/ff974821(v=vs.85).aspx) Article]

