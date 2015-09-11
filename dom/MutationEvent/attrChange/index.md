---
title: attrChange
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Mutation Events](https://developer.mozilla.org/en-US/docs/Web/Guide/Events/Mutation_events) Article]'
  - 'Microsoft Developer Network: [[event.attrChanged](http://msdn.microsoft.com/en-us/library/ie/ff974823(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/MutationEvent
    href: /dom/MutationEvent
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/MutationEvent
standardization_status: Deprecated
summary: 'Gets a value that indicates what type of change occurred.'
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
uri: dom/MutationEvent/attrChange

---
## <span>Summary</span>

Gets a value that indicates what type of change occurred.

Property of [dom/MutationEvent](/dom/MutationEvent)[dom/MutationEvent](/dom/MutationEvent)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var changeType = event.attrChange;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

One of the following numbers -

-   **1** - a modification occurred.
-   **2** - an addition occurred.
-   **3** - a removal occurred.

## <span>Related specifications</span>

[DOM Level 2 Events](http://www.w3.org/TR/DOM-Level-2-Events/)
:   Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Deprecated</span>

-   [-ms-radial-gradient](/css/properties/-ms-radial-gradient)

-   [-ms-repeating-linear-gradient](/css/properties/-ms-repeating-linear-gradient)

-   [-ms-repeating-radial-gradient](/css/properties/-ms-repeating-radial-gradient)

-   [MutationEvent](/dom/MutationEvent)

-   **attrChange**

-   [attrName](/dom/MutationEvent/attrName)

-   [initMutationEvent](/dom/MutationEvent/initMutationEvent)

-   [newValue](/dom/MutationEvent/newValue)

-   [prevValue](/dom/MutationEvent/prevValue)

-   [relatedNode](/dom/MutationEvent/relatedNode)

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [escape](/javascript/escape)

-   [unescape](/javascript/unescape)
