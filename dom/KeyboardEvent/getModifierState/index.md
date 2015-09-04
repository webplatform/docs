---
title: getModifierState
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'example/more description, compatibility'
summary: 'Queries the state of the specified modifier key.'
uri: dom/KeyboardEvent/getModifierState

---
# getModifierState

## Summary

Queries the state of the specified modifier key.

*Method of [dom/KeyboardEvent](/dom/KeyboardEvent)*

## Syntax

``` {.js}
var modifierState = event.getModifierState(modifierKeyName);
```

## Parameters

### modifierKeyName

 Data-typeÂ
:   String

 One of the following values -

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

## Return Value

Returns an object of type Boolean.

Whether the modifier key is active.

**Needs Examples**: This section should include examples.

## Notes

Some keyboard configurations contain a left and right modifier key. To determine whether the left or right key is pressed, use the [**location**](/dom/KeyboardEvent/location) property.

## Related specifications

Specification
:   Status
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

