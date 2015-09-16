---
title: 'MouseEvent'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[mouseEvent object](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent) Article]'
  - 'Microsoft Developer Network: [[mouseEvent object](http://msdn.microsoft.com/en-us/library/ie/ff974344(v=vs.85).aspx) Article]'
notes:
  - 'compatibility, possible examples/more detailed overview'
readiness: 'Almost Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: UIEvent
    href: /dom/UIEvent
standardization_status: 'W3C Working Draft'
summary: 'The DOM MouseEvent interface represents events that occur due to the user interacting with a pointing device (such as a mouse or touchpad).'
tags:
  - API
  - Objects
  - DOM
uri: dom/MouseEvent

---
## Summary

The DOM MouseEvent interface represents events that occur due to the user interacting with a pointing device (such as a mouse or touchpad).

Inherits from [UIEvent](/dom/UIEvent)[UIEvent](/dom/UIEvent)

## Properties

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

## Methods

API Name
:   Summary

[initMouseEvent](/dom/MouseEvent/initMouseEvent)
:   Initializes a new mouse event that the [**createEvent**](/dom/Document/createEvent) method created.

## Events

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

## Inherited from UIEvent

### Properties

API Name
:   Summary

[detail](/dom/UIEvent/detail)
:   Gets additional, developer defined, information about an event.

[view](/dom/UIEvent/view)
:   Gets the **window** object that an event is generated from.

    [object window]

### Methods

API Name
:   Summary

[initUIEvent](/dom/UIEvent/initUIEvent)
:   Initializes a new user interface event that the [createEvent](/dom/Document/createEvent) method created.

### Events

API Name
:   Summary

[abort](/dom/UIEvent/abort)
:   Fires when the user aborts the download.

[activate](/dom/UIEvent/activate)
:   Fires when the object is set as the active element.

**Needs Examples**: This section should include examples.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
