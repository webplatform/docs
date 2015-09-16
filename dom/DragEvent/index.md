---
title: 'DragEvent'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, compat'
readiness: 'In Progress'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: MouseEvent
    href: /dom/MouseEvent
standardization_status: 'W3C Candidate Recommendation'
tags:
  - API
  - Objects
  - DOM
uri: dom/DragEvent

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Inherits from [MouseEvent](/dom/MouseEvent)[MouseEvent](/dom/MouseEvent)

## Properties

API Name
:   Summary

[dataTransfer](/dom/DragEvent/dataTransfer)
:

## Methods

API Name
:   Summary

[initDragEvent](/dom/DragEvent/initDragEvent)
:   Initializes a new drag event.

## Events

API Name
:   Summary

[drag](/dom/DragEvent/drag)
:

[dragend](/dom/DragEvent/dragend)
:

[dragenter](/dom/DragEvent/dragenter)
:

[dragleave](/dom/DragEvent/dragleave)
:

[dragover](/dom/DragEvent/dragover)
:

[dragstart](/dom/DragEvent/dragstart)
:

[drop](/dom/DragEvent/drop)
:

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

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.9.2
