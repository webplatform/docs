---
title: 'setPointerCapture'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/library/ie/hh771882.aspx)'
notes:
  - 'Needs  examples, and compat'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
standardization_status: 'W3C Working Draft'
summary: 'Assigns a specified pointer to an element. This method is used to ensure that an element continues to receive pointer events even if the contact moves off the element.'
tags:
  - API_Object_Methods
  - Needs_Examples
uri: dom/Element/setPointerCapture

---
## Summary

Assigns a specified pointer to an element. This method is used to ensure that an element continues to receive pointer events even if the contact moves off the element.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
 element.setPointerCapture(pointerID);
```

## Parameters

### pointerID

 Data-type
:   Number

 The pointer to assign to the element.

## Return Value

No return value

## Usage

     Capturing the current pointer can improve usability by reducing the touch precision required when interacting with an element. For example, if a button is touched and held, and the user's finger slides off the button before raising it (breaking the contact), the button might not receive the pointerup event. This could cause the button to stay depressed forever. By assigning the pointer to the button element with setPointerCapture, the button receives pointer events, including the pointerup event that signals the button to return to its initial state.

The capture will be released when the pointer is removed (onpointerup) or explicitly released by calling the [releasePointerCapture](/dom/Element/releasePointerCapture) method. There are cases the element could lose the capture. For example, if the touch moves outside the window or some other element captures the touch, then the element that had the capture will lose the capture. The element that lost the capture will receive a [lostpointercapture](/dom/PointerEvent/lostpointercapture) event.

## Notes

When a pointer is captured to an element, the parent and ancestor elements receive a [gotpointercapture](/dom/PointerEvent/gotpointercapture) event during capture and bubble phase.

If the specified pointerId does not match any existing pointers, a [DOMException](/dom/DOMException) is thrown with the name *InvalidPointerId*.

## Related specifications

[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft

## See also

### Related articles

#### Pointer Events

-   [Pointer Events Primer](/concepts/Pointer_Events)

-   [releasePointerCapture](/dom/Element/releasePointerCapture)

-   **setPointerCapture**

-   [maxTouchPoints](/dom/Navigator/maxTouchPoints)

-   [pointerEnabled](/dom/Navigator/pointerEnabled)

-   [Introduction to multi-touch Web development](/tutorials/mobile_touch)

