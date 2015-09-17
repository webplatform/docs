---
title: 'WheelEvent'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[WheelEvent](https://developer.mozilla.org/en-US/docs/Web/API/WheelEvent) Article]'
  - 'Microsoft Developer Network: [[WheelEvent](http://msdn.microsoft.com/en-us/library/ie/ff974352(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: MouseEvent
    href: /dom/MouseEvent
standardization_status: 'W3C Working Draft'
summary: 'The DOM WheelEvent represents events that occur due to the user moving a mouse wheel or similar input device.'
tags:
  - API_Objects
  - DOM
uri: dom/WheelEvent

---
## Summary

The DOM WheelEvent represents events that occur due to the user moving a mouse wheel or similar input device.

Inherits from [MouseEvent](/dom/MouseEvent)[MouseEvent](/dom/MouseEvent)

## Properties

[deltaMode](/dom/WheelEvent/deltaMode)
:   Gets a value that indicates the unit of measurement for delta values.

[deltaX](/dom/WheelEvent/deltaX)
:   Gets the distance that a mouse wheel has rotated around the x-axis (horizontal).

[deltaY](/dom/WheelEvent/deltaY)
:   Gets the distance that a mouse wheel has rotated around the y-axis (vertical).

[deltaZ](/dom/WheelEvent/deltaZ)
:   Gets the distance that a mouse wheel has rotated around the z-axis.

## Methods

[initWheelEvent](/dom/WheelEvent/initWheelEvent)
:   Initializes a new WheelEvent that the createEvent method created.

## Events

*No events.*

## Inherited from MouseEvent

### Properties

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

[initMouseEvent](/dom/MouseEvent/initMouseEvent)
:   Initializes a new mouse event that the [**createEvent**](/dom/Document/createEvent) method created.

### Events

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

[detail](/dom/UIEvent/detail)
:   Gets additional, developer defined, information about an event.

[view](/dom/UIEvent/view)
:   Gets the **window** object that an event is generated from.

    [object window]

### Methods

[initUIEvent](/dom/UIEvent/initUIEvent)
:   Initializes a new user interface event that the [createEvent](/dom/Document/createEvent) method created.

### Events

[abort](/dom/UIEvent/abort)
:   Fires when the user aborts the download.

[activate](/dom/UIEvent/activate)
:   Fires when the object is set as the active element.

## Inherited from Event

### Properties

[bubbles](/dom/Event/bubbles)
:   Gets a value that indicates whether an event propagates up from the event target.

[cancelable](/dom/Event/cancelable)
:   Gets a value that indicates whether you can cancel an event's default action.

[currentTarget](/dom/Event/currentTarget)
:   Gets the event target that is currently being processed.

[defaultPrevented](/dom/Event/defaultPrevented)
:   Gets whether the default action should be canceled.

[eventPhase](/dom/Event/eventPhase)
:   Gets the event phase that is being evaluated.

[isTrusted](/dom/Event/isTrusted)
:   Gets a value that indicates whether a trusted event source created an event.

[target](/dom/Event/target)
:   Gets the element that is the original target of the event.

[timeStamp](/dom/Event/timeStamp)
:   Gets the time, in milliseconds, when an event occurred.

[type](/dom/Event/type)
:   Gets the name of an event.

### Methods

[initEvent](/dom/Event/initEvent)
:   Initializes a new generic event that the [**createEvent**](/dom/Document/createEvent) method created.

[preventDefault](/dom/Event/preventDefault)
:   Cancels the default action of an event, if possible.

[stopImmediatePropagation](/dom/Event/stopImmediatePropagation)
:   Prevents any further propagation of an event.

[stopPropagation](/dom/Event/stopPropagation)
:   Prevents propagation of an event beyond the current target.

### Events

[DOMContentLoaded](/dom/Event/DOMContentLoaded)
:

[afterprint](/dom/Event/afterprint)
:

[afterupdate](/dom/Event/afterupdate)
:

[beforeactivate](/dom/Event/beforeactivate)
:

[beforecopy](/dom/Event/beforecopy)
:

[beforecut](/dom/Event/beforecut)
:

[beforeeditfocus](/dom/Event/beforeeditfocus)
:

[beforepaste](/dom/Event/beforepaste)
:

[beforeprint](/dom/Event/beforeprint)
:

[beforeunload](/dom/Event/beforeunload)
:

[beforeupdate](/dom/Event/beforeupdate)
:

[bounce](/dom/Event/bounce)
:

[cellchange](/dom/Event/cellchange)
:

[change](/dom/Event/change)
:

[contextmenu](/dom/Event/contextmenu)
:

[controlselect](/dom/Event/controlselect)
:

[copy](/dom/Event/copy)
:

[cut](/dom/Event/cut)
:   Fires after a data selection is cut to the clipboard.

[dataavailable](/dom/Event/dataavailable)
:   Fires when new data at a data source becomes available.

[datasetchanged](/dom/Event/datasetchanged)
:   Fires when content at a data source has changed.

[datasetcomplete](/dom/Event/datasetcomplete)
:   Fires when data transfer from the data source has completed.

[deactivate](/dom/Event/deactivate)
:   Sets an active version of an object to not active.

[error](/dom/Event/error)
:   Fires when an error occurs.

[errorupdate](/dom/Event/errorupdate)
:   Executes any error handling associated with the event.

[filterchange](/dom/Event/filterchange)
:

[finish](/dom/Event/finish)
:

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
