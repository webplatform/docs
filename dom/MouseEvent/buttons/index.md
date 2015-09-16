---
title: 'buttons'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, compatibility'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/MouseEvent
    href: /dom/MouseEvent
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned short'
    href: /dom/MouseEvent
standardization_status: 'W3C Working Draft'
summary: 'Gets a value that indicates which mouse buttons a user pressed.'
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
uri: dom/MouseEvent/buttons

---
## Summary

Gets a value that indicates which mouse buttons a user pressed.

Property of [dom/MouseEvent](/dom/MouseEvent)[dom/MouseEvent](/dom/MouseEvent)

## Syntax

**Note**: This property is read-only.

``` js
var pressedButtons = event.buttons;
```

## Return Value

Returns an object of type unsigned shortunsigned short

A bitmask that represents the pressed mouse buttons.

-   0 - No button.
-   1 - The primary button (usually the left mouse button).
-   2 - The auxiliary button (usually the middle/wheel mouse button).
-   4 - The secondary button (usually the right mouse button).

Other values are always expressed as a power of 2, like 8, 16, 32 and so on and represent other buttons.

**Needs Examples**: This section should include examples.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
