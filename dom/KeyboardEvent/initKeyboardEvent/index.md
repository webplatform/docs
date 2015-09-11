---
title: initKeyboardEvent
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Technical review, compatibility, examples'
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/KeyboardEvent
    href: /dom/KeyboardEvent
standardization_status: 'W3C Working Draft'
summary: 'Initializes a new keyboard event that the  createEvent method created.'
tags:
  - API
  - Object
  - Methods
  - DOM
  - DOMEvents
uri: dom/KeyboardEvent/initKeyboardEvent

---
## <span>Summary</span>

Initializes a new keyboard event that the createEvent method created.

Method of [dom/KeyboardEvent](/dom/KeyboardEvent)[dom/KeyboardEvent](/dom/KeyboardEvent)

## <span>Syntax</span>

``` js
 event.initKeyboardEvent(eventType, canBubble, cancelable, view, key, location, modifiersList, repeat, locale);
```

## <span>Parameters</span>

### <span>eventType</span>

 Data-type
:   String

 The name of the event. Sets the value for the [**type**](/dom/Event/type) property.

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

### <span>key</span>

 Data-type
:   Number

 The **key identifier**. Sets the value for the [**key**](/dom/KeyboardEvent/key) property.

### <span>location</span>

 Data-type
:   Number

 The location of the key on the device. Sets the value for the [**location**](/dom/KeyboardEvent/location) property.

### <span>modifiersList</span>

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

### <span>repeat</span>

 Data-type
:   Number

 The number of times this key has been pressed. Sets the value for the [**repeat**](/dom/KeyboardEvent/repeat) property.

### <span>locale</span>

 Data-type
:   String

 The locale name. Sets the value for the [**locale**](/dom/CompositionEvent/locale) property.

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Notes</span>

The information in this page corresponds to the 20100908 outdated working draft edition of the specifications.

## <span>Related specifications</span>

[DOM Level 3 Events (20090908)](http://www.w3.org/TR/2009/WD-DOM-Level-3-Events-20090908/)
:   Outdated Working Draft

[DOM Level 3 Events (20100907)](http://www.w3.org/TR/2010/WD-DOM-Level-3-Events-20100907/)
:   Outdated Working Draft
