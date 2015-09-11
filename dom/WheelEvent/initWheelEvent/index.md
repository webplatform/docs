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
## <span>Summary</span>

Initializes a new WheelEvent that the createEvent method created.

Method of [dom/WheelEvent](/dom/WheelEvent)[dom/WheelEvent](/dom/WheelEvent)

## <span>Syntax</span>

``` js
 event.initWheelEvent(/* see parameter list */);
```

## <span>Parameters</span>

### <span>eventType</span>

 Data-type
:   String

 The name of the event. Sets the value for the [type](/dom/Event/type) property.

### <span>canBubble</span>

 Data-type
:   Boolean

 Whether the event propagates upward. Sets the value for the [bubbles](/dom/Event/bubbles) property.

### <span>cancelable</span>

 Data-type
:   Boolean

 Whether the event is cancelable and so [preventDefault](/dom/Event/preventDefault) can be called. Sets the value for the [cancelable](/dom/Event/cancelable) property.

### <span>view</span>

 Data-type
:   Object

 The window on which this event is occurring. Sets the value for the [view](/dom/UIEvent/view) property.

### <span>detail</span>

 Data-type
:   Number

 Specifies additional information. This value is returned in the [**detail**](/dom/UIEvent/detail) property of the event.

### <span>screenX</span>

 Data-type
:   Number

 The x-coordinate of the mouse pointer, relative to the upper-left corner of the screen. Sets the value for the [**screenX**](/dom/MouseEvent/screenX) property,

### <span>screenY</span>

 Data-type
:   Number

 The y-coordinate of the mouse pointer, relative to the upper-left corner of the screen. Sets the value for the [**screenY**](/dom/MouseEvent/screenY) property.

### <span>clientX</span>

 Data-type
:   Number

 The x-coordinate of the mouse pointer, relative to the upper-left corner of the browser's client area. Sets the value for the [**clientX**](/dom/MouseEvent/clientX) property.

### <span>clientY</span>

 Data-type
:   any

 The y-coordinate of the mouse pointer, relative to the upper-left corner of the browser's client area. Sets the value for the [**clientY**](/dom/MouseEvent/clientY) property.

### <span>button</span>

 Data-type
:   Number

 The mouse button that caused the event. Sets the value for the [**button**](/dom/MouseEvent/button) property (see the property page for common values).

### <span>relatedTarget</span>

 Data-type
:   DOM Node

 A secondary element that is involved in the event. Sets the value for the [**relatedTarget**](/dom/MouseEvent/relatedTarget) property.

### <span>modifiersListArg</span>

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

### <span>deltaX</span>

 Data-type
:   Number

 The distance that the mouse wheel has rotated around the x-axis. Sets the value for the [**deltaX**](/dom/WheelEvent/deltaX) property.

### <span>deltaY</span>

 Data-type
:   Number

 The distance that the mouse wheel has rotated around the y-axis. Sets the value for the [**deltaY**](/dom/WheelEvent/deltaY) property.

### <span>deltaZ</span>

 Data-type
:   Number

 The distance that the mouse wheel has rotated around the z-axis. Sets the value for the [**deltaZ**](/dom/WheelEvent/deltaZ) property.

### <span>deltaMode</span>

 Data-type
:   Number

 The delta mode of the event. Sets the value for the [**deltaMode**](/dom/WheelEvent/deltaMode) property (see the property page for common values).

## <span>Return Value</span>

No return value

## <span>Examples</span>

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

## <span>Related specifications</span>

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
