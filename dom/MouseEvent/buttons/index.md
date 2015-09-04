---
title: buttons
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'examples, compatibility'
summary: 'Gets a value that indicates which mouse buttons a user pressed.'
uri: dom/MouseEvent/buttons

---
# buttons

## Summary

Gets a value that indicates which mouse buttons a user pressed.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/MouseEvent](/dom/MouseEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var pressedButtons = event.buttons;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned short</span></span>

A bitmask that represents the pressed mouse buttons.

-   0 - No button.
-   1 - The primary button (usually the left mouse button).
-   2 - The auxiliary button (usually the middle/wheel mouse button).
-   4 - The secondary button (usually the right mouse button).

Other values are always expressed as a power of 2, like 8, 16, 32 and so on and represent other buttons.

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

