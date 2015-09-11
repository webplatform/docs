---
title: pointerId
attributions:
  - 'Microsoft Developer Network: [[pointerId Property](http://msdn.microsoft.com/en-us/library/ie/hh772358(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/PointerEvent
    href: /dom/PointerEvent
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /dom/PointerEvent
standardization_status: 'W3C Working Draft'
summary: 'A unique identifier for the pointer causing the event'
tags:
  - API
  - Object
  - Properties
uri: dom/PointerEvent/pointerId

---
## <span>Summary</span>

A unique identifier for the pointer causing the event

Property of [dom/PointerEvent](/dom/PointerEvent)[dom/PointerEvent](/dom/PointerEvent)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = event.pointerId;
```

## <span>Return Value</span>

Returns an object of type unsigned longunsigned long

The unique identifier of the contact for a touch, mouse or pen.

## <span>Examples</span>

``` js
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

## <span>Usage</span>

     This identifier must be unique from all other active pointers at the time. A user agent may recycle previously retired values for pointerId from previous active pointers, if necessary.

If the device producing the event is a mouse, then the pointerId must be 1. Device types other than mouse must not have a pointerId of 1.

