---
title: root
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NodeIterator.root](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.root) Article]'
  - 'Microsoft Developer Network: [[root Property](http://msdn.microsoft.com/en-us/library/ie/ff974821(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/NodeIterator
    href: /dom/NodeIterator
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/NodeIterator
standardization_status: 'W3C Recommendation'
summary: 'The NodeIterator.root read-only property represents the Node that is the root of what the NodeIterator traverses.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/NodeIterator/root

---
## Summary

The NodeIterator.root read-only property represents the Node that is the root of what the NodeIterator traverses.

Property of [dom/NodeIterator](/dom/NodeIterator)[dom/NodeIterator](/dom/NodeIterator)

## Syntax

**Note**: This property is read-only.

``` js
var node = element.root;
```

## Return Value

Returns an object of type DOM NodeDOM Node

## Examples

``` js
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

[DOM](http://dom.spec.whatwg.org/#dom-nodeiterator-root)
:   Living Standard
