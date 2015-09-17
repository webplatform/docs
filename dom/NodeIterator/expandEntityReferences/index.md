---
title: 'expandEntityReferences'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NodeIterator.explandEntityReferences](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.expandEntityReferences) Article]'
  - 'Microsoft Developer Network: [[expandEntityReferences Property](http://msdn.microsoft.com/en-us/library/ie/ff974819(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/NodeIterator
    href: /dom/NodeIterator
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/NodeIterator
standardization_status: Deprecated
summary: 'Flag to specify whether or not the children of entity reference nodes are visible. '
tags:
  - API_Object_Properties
  - DOM
uri: dom/NodeIterator/expandEntityReferences

---
## Summary

Flag to specify whether or not the children of entity reference nodes are visible.

Property of [dom/NodeIterator](/dom/NodeIterator)[dom/NodeIterator](/dom/NodeIterator)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.expandEntityReferences;
```

## Return Value

Returns an object of type BooleanBoolean

The NodeIterator.expandEntityReferences read-only property returns a Boolean flag indicating whether or not the children of entity reference nodes are visible to the NodeIterator.

If this value is false, the children of entity reference nodes (as well as all of their descendants) are rejected. This takes precedence over the value of the NodeIterator.whatToShow method and the associated filter.

## Examples

``` js
var nodeIterator = document.createNodeIterator(
    document.body,
    NodeFilter.SHOW_ELEMENT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false
);
expand = nodeIterator.expandEntityReferences;
```

## Notes

### Remarks

Deprecated

This feature has been removed from the Web. Though some browsers may still support it, it is in the process of being dropped. Do not use it in old or new projects. Pages or Web apps using it may break at any time.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 1.2

## Related specifications

[DOM](http://dom.spec.whatwg.org/#nodeiterator)
:   Living Standard
