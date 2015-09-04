---
title: initKeyboardEvent
tags:
  - API
  - Object
  - Methods
  - DOM
  - DOMEvents
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
notes:
  - 'Technical review, compatibility, examples'
summary: 'Initializes a new keyboard event that the  createEvent method created.'
uri: dom/KeyboardEvent/initKeyboardEvent

---
# initKeyboardEvent

## Summary

Initializes a new keyboard event that the createEvent method created.

*Method of [dom/KeyboardEvent](/dom/KeyboardEvent)*

## Syntax

``` {.js}
 event.initKeyboardEvent(eventType, canBubble, cancelable, view, key, location, modifiersList, repeat, locale);
```

## Parameters

### eventType

 Data-typeÂ
:   String

 The name of the event. Sets the value for the [**type**](/dom/Event/type) property.

### canBubble

 Data-typeÂ
:   Boolean

 Whether the event propagates upward. Sets the value for the [bubbles](/dom/Event/bubbles) property.

### cancelable

 Data-typeÂ
:   Boolean

 Whether the event is cancelable and so [preventDefault](/dom/Event/preventDefault) can be called. Sets the value for the [cancelable](/dom/Event/cancelable) property.

### view

 Data-typeÂ
:   Object

 The window on which this event is occurring. Sets the value for the [view](/dom/UIEvent/view) property.

### key

 Data-typeÂ
:   Number

 The **key identifier**. Sets the value for the [**key**](/dom/KeyboardEvent/key) property.

### location

 Data-typeÂ
:   Number

 The location of the key on the device. Sets the value for the [**location**](/dom/KeyboardEvent/location) property.

### modifiersList

 Data-typeÂ
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

### repeat

 Data-typeÂ
:   Number

 The number of times this key has been pressed. Sets the value for the [**repeat**](/dom/KeyboardEvent/repeat) property.

### locale

 Data-typeÂ
:   String

 The locale name. Sets the value for the [**locale**](/dom/CompositionEvent/locale) property.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

The information in this page corresponds to the 20100908 outdated working draft edition of the specifications.

## Related specifications

Specification
:   Status
[DOM Level 3 Events (20090908)](http://www.w3.org/TR/2009/WD-DOM-Level-3-Events-20090908/)
:   Outdated Working Draft
[DOM Level 3 Events (20100907)](http://www.w3.org/TR/2010/WD-DOM-Level-3-Events-20100907/)
:   Outdated Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

