---
title: releasePointerCapture
notes:
  - 'Needs examples and compat'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
standardization_status: 'W3C Working Draft'
summary: 'Releases a pointer captured by an element (using the setPointerCapture method).'
tags:
  - API
  - Object
  - Methods
uri: dom/Element/releasePointerCapture

---
## Summary

Releases a pointer captured by an element (using the setPointerCapture method).

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
 element.releasePointerCapture(pointerId);
```

## Parameters

### pointerId

 Data-type
:   Number

 Identifier of the pointer to be released.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

If the specified pointerId does not match any existing pointers, a [DOMException](/dom/DOMException) is thrown with the name *InvalidPointerId*.

## Related specifications

[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft

## See also

### Related articles

#### Pointer Events

-   [Pointer Events Primer](/concepts/Pointer_Events)

-   **releasePointerCapture**

-   [setPointerCapture](/dom/Element/setPointerCapture)

-   [maxTouchPoints](/dom/Navigator/maxTouchPoints)

-   [pointerEnabled](/dom/Navigator/pointerEnabled)

-   [Introduction to multi-touch Web development](/tutorials/mobile_touch)

