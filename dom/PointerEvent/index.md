---
title: PointerEvent
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[PointerEvent(under construction)](https://developer.mozilla.org/en-US/docs/Web/API/PointerEvent) Article]'
  - 'Microsoft Developer Network: [[PointerEvent Object](http://msdn.microsoft.com/en-us/library/ie/hh772103(v=vs.85).aspx) Article]'
notes:
  - "No MDN documentation....\nMy example needs uploading by Renoir"
readiness: 'Almost Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: MouseEvent
    href: /dom/MouseEvent
standardization_status: 'W3C Working Draft'
summary: 'Provides contextual information associated with input events (for example, from mouse, touch or pen).'
tags:
  - API
  - Objects
uri: dom/PointerEvent

---
## Summary

Provides contextual information associated with input events (for example, from mouse, touch or pen).

Inherits from [MouseEvent](/dom/MouseEvent)[MouseEvent](/dom/MouseEvent)

## Properties

API Name
:   Summary

[height](/dom/PointerEvent/height)
:   The height (magnitude on the Y axis), in CSS pixels, of the contact geometry of the pointer.

[isPrimary](/dom/PointerEvent/isPrimary)
:   Returns whether the pointer associated with the event is the primary pointer for the current mouse, touch, or pen interaction.

[pointerId](/dom/PointerEvent/pointerId)
:   A unique identifier for the pointer causing the event

[pointerType](/dom/PointerEvent/pointerType)
:   Indicates the device type that caused the event (mouse, pen, touch, etc.).

[pressure](/dom/PointerEvent/pressure)
:   The normalized pressure of the pointer input in the range of [0,1], where 0 and 1 represent the minimum and maximum pressure the hardware is capable of detecting, respectively.

[tiltX](/dom/PointerEvent/tiltX)
:   The plane angle (in degrees, in the range of [-90,90]) between the Y-Z plane and the plane containing both the transducer (e.g. pen stylus) axis and the Y axis.

[tiltY](/dom/PointerEvent/tiltY)
:   The plane angle (in degrees, in the range of [-90,90]) between the X-Z plane and the plane containing both the transducer (e.g. pen stylus) axis and the X axis.

[width](/dom/PointerEvent/width)
:   The width (magnitude on the X axis), in CSS pixels, of the contact geometry of the pointer.

## Methods

API Name
:   Summary

[initPointerEvent](/dom/PointerEvent/initPointerEvent)
:   Initializes a new **PointerEvent** created by the [createEvent](/dom/Document/createEvent) method.

## Events

API Name
:   Summary

[gotpointercapture](/dom/PointerEvent/gotpointercapture)
:   Dispatched prior to the dispatch of the first event after pointer capture is set for a pointer. See the **PointerEvent** object.

[lostpointercapture](/dom/PointerEvent/lostpointercapture)
:   Dispatched after pointer capture is released for a pointer.

[pointercancel](/dom/PointerEvent/pointercancel)
:   Dispatched when either (1) the user agent has determined that a pointer is unlikely to continue to produce events (e.g., due to a hardware event), or (2) after having fired the [pointerdown](/dom/PointerEvent/pointerdown) event, the pointer is subsequently used to manipulate the page viewport (e.g., panning or zooming).

[pointerdown](/dom/PointerEvent/pointerdown)
:   Dispatched when a pointer enters the state of having a non-zero value for the [buttons](/dom/MouseEvent/buttons) property.

[pointerenter](/dom/PointerEvent/pointerenter)
:   Dispatched when a pointing device is moved into the hit test boundaries of an element or one of its descendants, including as a result of a [pointerdown](/dom/PointerEvent/pointerdown) event from a device that does not support hover.

[pointerleave](/dom/PointerEvent/pointerleave)
:   Dispatched when a pointing device is moved off of the hit test boundaries of an element and all of its descendants, including as a result of a [pointerup](/dom/PointerEvent/pointerup) event from a device that does not support hover.

[pointermove](/dom/PointerEvent/pointermove)
:   Dispatched when a pointer changes coordinates, button state, pressure, tilt, or contact geometry (e.g. [width](/dom/PointerEvent/width) and [height](/dom/PointerEvent/height)).

[pointerout](/dom/PointerEvent/pointerout)
:   Dispatched when any of the following occurs:
    -   A pointing device is moved out of the hit test boundaries of an element
    -   After firing the [pointerup](/dom/PointerEvent/pointerup) event for a device that does not support hover
    -   After firing the [pointercancel](/dom/PointerEvent/pointercancel) event

[pointerover](/dom/PointerEvent/pointerover)
:   Dispatched when a pointing device is moved into the hit test boundaries of an element. Also dispatched prior to a [pointerdown](/dom/PointerEvent/pointerdown) event for devices that do not support hover.

[pointerup](/dom/PointerEvent/pointerup)
:   Dispatched when a pointer leaves the state of having a non-zero value for the [buttons](/dom/MouseEvent/buttons) property.

## Inherited from MouseEvent

### Properties

API Name
:   Summary

[button](/dom/MouseEvent/button)
:   Gets the mouse button that caused an event.

[buttons](/dom/MouseEvent/buttons)
:   Gets a value that indicates which mouse buttons a user pressed.

[clientX](/dom/MouseEvent/clientX)
:   Gets the x-coordinate of the mouse pointer, relative to the upper-left corner of the viewport (that is, the user agent's client area).

[clientY](/dom/MouseEvent/clientY)
:   Gets the y-coordinate of the mouse pointer, relative to the upper-left corner of the viewport (that is, the user agent's client area).

[layerX](/dom/MouseEvent/layerX)
:   Gets the x-coordinate of the mouse pointer, relative to the last positioned ancestor element.

[layerY](/dom/MouseEvent/layerY)
:   Returns the horizontal coordinate of the event relative to the current layer.

    layerY is a non-standards property of the MouseEvent object.

[relatedTarget](/dom/MouseEvent/relatedTarget)
:   Gets the secondary element that is involved in an event.

    The relatedTarget property is used to find the other element, if any, involved in an event. Events like mouseover are oriented around a certain target, but also involve a secondary target, such as the target that is exited as the mouseover event fires for the primary target.

[screenX](/dom/MouseEvent/screenX)
:   Gets the x-coordinate of the mouse pointer, relative to the upper-left corner of the screen.

[screenY](/dom/MouseEvent/screenY)
:   Gets the y-coordinate of the mouse pointer, relative to the upper-left corner of the screen.

[x](/dom/MouseEvent/x)
:   Gets the x-coordinate of the mouse cursor, relative to the last positioned ancestor element.

[y](/dom/MouseEvent/y)
:   Gets the y-coordinate of the mouse pointer, relative to the last positioned ancestor element.

### Methods

API Name
:   Summary

[initMouseEvent](/dom/MouseEvent/initMouseEvent)
:   Initializes a new mouse event that the [**createEvent**](/dom/Document/createEvent) method created.

### Events

API Name
:   Summary

[click](/dom/MouseEvent/click)
:   The click event is triggered for an element when it is activated by a mouse click or by another user action that normally has the same effect as a mouse click.

[dblclick](/dom/MouseEvent/dblclick)
:   A mouse double click event.

[mousedown](/dom/MouseEvent/mousedown)
:   Fires when the user clicks the object with either mouse button or taps the mouse pad.

[mouseenter](/dom/MouseEvent/mouseenter)
:   Fires when the user moves the mouse pointer into the object.

[mouseleave](/dom/MouseEvent/mouseleave)
:   Fires when the user moves the mouse pointer outside the boundaries of the object.

[mousemove](/dom/MouseEvent/mousemove)
:   Fires when the user moves the mouse over the object.

[mouseout](/dom/MouseEvent/mouseout)
:   Fires when the user moves the mouse pointer outside the boundaries of the object.

[mouseover](/dom/MouseEvent/mouseover)
:   Fires when the user moves the mouse pointer into the object.

[mouseup](/dom/MouseEvent/mouseup)
:   Fires when the user releases a mouse button while the mouse is over the object.

**Needs Examples**: This section should include examples.

## Related specifications

[Pointer Events](http://www.w3.org/TR/pointerevents/)
:   Working Draft

## See also

### Related articles

#### Pointer Events

-   [Pointer Events Primer](/concepts/Pointer_Events)

-   [releasePointerCapture](/dom/Element/releasePointerCapture)

-   [setPointerCapture](/dom/Element/setPointerCapture)

-   [maxTouchPoints](/dom/Navigator/maxTouchPoints)

-   [pointerEnabled](/dom/Navigator/pointerEnabled)

-   [Introduction to multi-touch Web development](/tutorials/mobile_touch)

