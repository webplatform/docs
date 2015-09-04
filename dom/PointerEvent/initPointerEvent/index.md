---
title: initPointerEvent
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Initializes a new PointerEvent created by the createEvent method.'
uri: dom/PointerEvent/initPointerEvent

---
# initPointerEvent

## Summary

Initializes a new PointerEvent created by the createEvent method.

*Method of [dom/PointerEvent](/dom/PointerEvent)*

## Syntax

``` {.js}
 event.initPointerEvent(/* see parameter list */);
```

## Parameters

### type

 Data-typeÂ
:   String

 The type of the event being created, such as: pointerdown, pointerup, pointercancel, pointermove, pointerover, pointerout, pointerenter, pointerleave, gotpointercapture, lostpointercapture.

### canBubble

 Data-typeÂ
:   Boolean

 Indicates whether the event can bubble. When true, the event should propagate upward. When false, the event does not propagate upward.

### cancelable

 Data-typeÂ
:   Boolean

 Indicates whether the eventâ€™s default action can be prevented. When true, the default action can be canceled. When false, the default action cannot be canceled.

### view

 Data-typeÂ
:   any

 The view in which the event is taking place.

### detail

 Data-typeÂ
:   Number

 Specifies some detailed information depending upon the event.

### screenX

 Data-typeÂ
:   Number

 The x-coordinate of the event in screen coordinates relative to the upper left corner of the screen.

### screenY

 Data-typeÂ
:   Number

 The y-coordinate of the event in screen coordinates relative to the upper left corner of the screen.

### clientX

 Data-typeÂ
:   Number

 The x-coordinate of the event in client coordinates relative to the upper-left corner of the document's client area.

### clientY

 Data-typeÂ
:   Number

 The y-coordinate of the event in client coordinates relative to the upper-left corner of the document's client area.

### ctrlKey

 Data-typeÂ
:   Boolean

 Indicates the state of the Ctrl key. When true, the left or right Ctrl key is pressed. If false, neither Ctrl key is pressed.

### altKey

 Data-typeÂ
:   Boolean

 Indicates the state of the Alt key. When true, the left or right Alt key is pressed. If false, neither Alt key is pressed.

### shiftKey

 Data-typeÂ
:   Boolean

 Indicates the state of the Shift key. When true, the left or right Shift key is pressed. If false, neither Shift key is pressed.

### metaKey

 Data-typeÂ
:   Boolean

 Indicates the state of the Meta/Command key. If true, the left or right Meta/Command key is pressed. If false neither Meta/Command key is pressed.

### button

 Data-typeÂ
:   Number

 If the event is caused by a mouse event, this indicates the mouse button that caused the event.

### relatedTarget

 Data-typeÂ
:   any

 A reference to the related element.

### offsetX

 Data-typeÂ
:   Number

 The x-coordinate of the event in the element.

### offsetY

 Data-typeÂ
:   Number

 The y-coordinate of the event in the element.

### width

 Data-typeÂ
:   Number

 The contact width of the pointer point specified by pointerId. Default: 0

### height

 Data-typeÂ
:   Number

 The contact height of the pointer point specified by pointerId. Default: 0

### pressure

 Data-typeÂ
:   Number

 Pen pressure normalized in a range of 0 to 255. Default: 0

### tiltX

 Data-typeÂ
:   Number

 The plane angle between the Y-Z plane and the plane containing the transducer axis and the Y axis. A positive X Tilt is to the right.

This quantity is used in conjunction with Y Tilt to represent the tilt away from normal of a transducer, such as a stylus.

Range: -90 to +90 Default: 0

### tiltY

 Data-typeÂ
:   Number

 Represents the angle between the X-Z and transducer-X planes.

A positive Y Tilt is toward the user.

Range: -90 to +90 Default: 0

### pointerId

 Data-typeÂ
:   Number

 Specifies the unique ID of the contact. Default: 0

### pointerType

 Data-typeÂ
:   String

 Indicates whether the source is touch, pen or mouse. Default: ""

### isPrimary

 Data-typeÂ
:   Boolean

 Indicates whether this is the primary pointer that is used to control the mouse position in a multi-touch scenario. Default: false

## Return Value

No return value

## Examples

``` {.js}
var retval = PointerEvent.initPointerEvent(typeArg, canBubbleArg, cancelableArg, viewArg, detailArg, screenXArg, screenYArg, clientXArg, clientYArg, ctrlKeyArg, altKeyArg, shiftKeyArg, metaKeyArg, buttonArg, relatedTargetArg, offsetXArg, offsetYArg, widthArg, heightArg, pressure, rotation, tiltX, tiltY, pointerIdArg, pointerType, hwTimestampArg, isPrimary);
```

### Syntax

## Related specifications

Specification
:   Status
[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft

## See also

### External resources

-   [Pointer Events, Section 3.1.3: PointerEvent Constructor](http://www.w3.org/TR/pointerevents/#pointerevent-constructor)
-   [Pointer Events, Section 9: Dispatching an untrusted pointer event example](http://www.w3.org/TR/pointerevents/#examples)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[initPointerEvent Method](http://msdn.microsoft.com/en-us/library/ie/hh772109(v=vs.85).aspx) Article]

