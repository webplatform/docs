---
title: pointerId
tags:
  - API
  - Object
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'A unique identifier for the pointer causing the event'
uri: dom/PointerEvent/pointerId

---
# pointerId

## Summary

A unique identifier for the pointer causing the event

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/PointerEvent](/dom/PointerEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = event.pointerId;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

The unique identifier of the contact for a touch, mouse or pen.

## Examples

``` {.js}
//  Adds a pointer to the MSGesture object for the red square
function redListener(evt)
{
    if (evt.type == "pointerdown")
    {
        redGesture.addPointer(evt.pointerId);
        return;
    }
    printEvent(evt);
}
```

## Usage

     This identifier must be unique from all other active pointers at the time. A user agent may recycle previously retired values for pointerId from previous active pointers, if necessary.

If the device producing the event is a mouse, then the pointerId must be 1. Device types other than mouse must not have a pointerId of 1.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[pointerId Property](http://msdn.microsoft.com/en-us/library/ie/hh772358(v=vs.85).aspx) Article]

