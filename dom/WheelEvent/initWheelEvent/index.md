---
title: initWheelEvent
attributions:
  - 'Microsoft Developer Network: [[initWheelEvent](http://msdn.microsoft.com/en-us/library/ie/ff975254(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/WheelEvent
    href: /dom/WheelEvent
summary: 'Initializes a new WheelEvent that the createEvent method created.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/WheelEvent/initWheelEvent

---
## Summary

Initializes a new WheelEvent that the createEvent method created.

Method of [dom/WheelEvent](/dom/WheelEvent)[dom/WheelEvent](/dom/WheelEvent)

## Syntax

``` js
 event.initWheelEvent(/* see parameter list */);
```

## Parameters

### eventType

 Data-type
:   String

 The name of the event. Sets the value for the [type](/dom/Event/type) property.

### canBubble

 Data-type
:   Boolean

 Whether the event propagates upward. Sets the value for the [bubbles](/dom/Event/bubbles) property.

### cancelable

 Data-type
:   Boolean

 Whether the event is cancelable and so [preventDefault](/dom/Event/preventDefault) can be called. Sets the value for the [cancelable](/dom/Event/cancelable) property.

### view

 Data-type
:   Object

 The window on which this event is occurring. Sets the value for the [view](/dom/UIEvent/view) property.

### detail

 Data-type
:   Number

 Specifies additional information. This value is returned in the [**detail**](/dom/UIEvent/detail) property of the event.

### screenX

 Data-type
:   Number

 The x-coordinate of the mouse pointer, relative to the upper-left corner of the screen. Sets the value for the [**screenX**](/dom/MouseEvent/screenX) property,

### screenY

 Data-type
:   Number

 The y-coordinate of the mouse pointer, relative to the upper-left corner of the screen. Sets the value for the [**screenY**](/dom/MouseEvent/screenY) property.

### clientX

 Data-type
:   Number

 The x-coordinate of the mouse pointer, relative to the upper-left corner of the browser's client area. Sets the value for the [**clientX**](/dom/MouseEvent/clientX) property.

### clientY

 Data-type
:   any

 The y-coordinate of the mouse pointer, relative to the upper-left corner of the browser's client area. Sets the value for the [**clientY**](/dom/MouseEvent/clientY) property.

### button

 Data-type
:   Number

 The mouse button that caused the event. Sets the value for the [**button**](/dom/MouseEvent/button) property (see the property page for common values).

### relatedTarget

 Data-type
:   DOM Node

 A secondary element that is involved in the event. Sets the value for the [**relatedTarget**](/dom/MouseEvent/relatedTarget) property.

### modifiersListArg

 Data-type
:   String

 A space-separated list of any of the following values:

-   **Alt** - The left or right Alt key.
-   **AltGraph** - The Ctrl and Alt keys.
-   **CapsLock** - The Caps Lock toggle.
-   **Control** - The left or right Ctrl key.
-   **Meta** - The Meta/Control key.
-   **NumLock** - The Num Lock toggle.
-   **ScrollLock** - The Scroll Lock toggle.
-   **Shift** - The left or right Shift key.
-   **Fn**
-   **OS**
-   **SymbolLock**

Other implementation specific options may be supported. For example -

-   **Win** (on Microsoft Windows) - The left or right Windows logo key.
-   **Scroll** - The Scroll Lock toggle.

### deltaX

 Data-type
:   Number

 The distance that the mouse wheel has rotated around the x-axis. Sets the value for the [**deltaX**](/dom/WheelEvent/deltaX) property.

### deltaY

 Data-type
:   Number

 The distance that the mouse wheel has rotated around the y-axis. Sets the value for the [**deltaY**](/dom/WheelEvent/deltaY) property.

### deltaZ

 Data-type
:   Number

 The distance that the mouse wheel has rotated around the z-axis. Sets the value for the [**deltaZ**](/dom/WheelEvent/deltaZ) property.

### deltaMode

 Data-type
:   Number

 The delta mode of the event. Sets the value for the [**deltaMode**](/dom/WheelEvent/deltaMode) property (see the property page for common values).

## Return Value

No return value

## Examples

``` js
function dispatchWheelEvent(){
        var evt=document.createEvent('WheelEvent');
        var theform=document.forms.dispatch;
        //var retval = WheelEvent.initWheelEvent(eventType, canBubble, cancelable, view, detail, screenXArg, screenYArg, clientXArg, clientYArg, buttonArg, relatedTargetArg, modifiersListArg, deltaX, deltaY, deltaZ, deltaMode);
        evt.initWheelEvent('wheel',
                            theform.chkcanbubble.checked,
                            theform.chkcancellable.checked,
                            eval(theform.view.value),
                            theform.detail.value,
                            theform.screenx.value,
                            theform.screeny.value,
                            theform.clientx.value,
                            theform.clienty.value,
                            theform.button.value,
                            null,
                            theform.modifierlist.value,
                            theform.deltax.value,
                            theform.deltay.value,
                            theform.deltaz.value,
                            theform.cbodeltamode.value);


        window.dispatchEvent(evt);
   }
```

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
