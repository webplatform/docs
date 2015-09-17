---
title: 'relatedNode'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Mutation Events](https://developer.mozilla.org/en-US/docs/Web/Guide/Events/Mutation_events) Article]'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/MutationEvent
    href: /dom/MutationEvent
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/MutationEvent
standardization_status: Deprecated
summary: 'Gets a second node related to a mutation event.'
tags:
  - API_Object_Properties
  - DOM
  - DOMEvents
uri: dom/MutationEvent/relatedNode

---
## Summary

Gets a second node related to a mutation event.

Property of [dom/MutationEvent](/dom/MutationEvent)[dom/MutationEvent](/dom/MutationEvent)

## Syntax

**Note**: This property is read-only.

``` js
var relatedNode = event.relatedNode;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The second node related to the event.

## Notes

In a `DOMAttrModified` event, the related node is the attribute node that is being modified. In a `DOMNodeInserted` or `DOMNodeRemoved` event, the related node is the parent node of the event target.

## Related specifications

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
