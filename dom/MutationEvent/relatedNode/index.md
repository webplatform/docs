---
title: relatedNode
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
readiness: 'Ready to Use'
standardization_status: Deprecated
summary: 'Gets a second node related to a mutation event.'
uri: dom/MutationEvent/relatedNode

---
# relatedNode

## Summary

Gets a second node related to a mutation event.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/MutationEvent](/dom/MutationEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var relatedNode = event.relatedNode;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

The second node related to the event.

## Notes

In a `DOMAttrModified` event, the related node is the attribute node that is being modified. In a `DOMNodeInserted` or `DOMNodeRemoved` event, the related node is the parent node of the event target.

## Related specifications

Specification
:   Status
[DOM Level 2 Events](http://www.w3.org/TR/DOM-Level-2-Events/)
:   Recommendation

## See also

### Related articles

#### Deprecated

-   [-ms-radial-gradient](/css/properties/-ms-radial-gradient)

-   [-ms-repeating-linear-gradient](/css/properties/-ms-repeating-linear-gradient)

-   [-ms-repeating-radial-gradient](/css/properties/-ms-repeating-radial-gradient)

-   [MutationEvent](/dom/MutationEvent)

-   [attrChange](/dom/MutationEvent/attrChange)

-   [attrName](/dom/MutationEvent/attrName)

-   [initMutationEvent](/dom/MutationEvent/initMutationEvent)

-   [newValue](/dom/MutationEvent/newValue)

-   [prevValue](/dom/MutationEvent/prevValue)

-   **relatedNode**

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [escape](/javascript/escape)

-   [unescape](/javascript/unescape)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Mutation Events](https://developer.mozilla.org/en-US/docs/Web/Guide/Events/Mutation_events) Article]

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

