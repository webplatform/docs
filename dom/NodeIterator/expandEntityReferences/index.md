---
title: expandEntityReferences
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: Deprecated
summary: 'Flag to specify whether or not the children of entity reference nodes are visible. '
uri: dom/NodeIterator/expandEntityReferences

---
# expandEntityReferences

## Summary

Flag to specify whether or not the children of entity reference nodes are visible.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/NodeIterator](/dom/NodeIterator)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.expandEntityReferences;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

The NodeIterator.expandEntityReferences read-only property returns a Boolean flag indicating whether or not the children of entity reference nodes are visible to the NodeIterator.

If this value is false, the children of entity reference nodes (as well as all of their descendants) are rejected. This takes precedence over the value of the NodeIterator.whatToShow method and the associated filter.

## Examples

``` {.js}
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

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#nodeiterator)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NodeIterator.explandEntityReferences](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.expandEntityReferences) Article]

Portions of this content come from the Microsoft Developer Network: [[expandEntityReferences Property](http://msdn.microsoft.com/en-us/library/ie/ff974819(v=vs.85).aspx) Article]

