---
title: button
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'examples, compatibility, more info'
summary: 'Gets the mouse button that caused an event.'
uri: dom/MouseEvent/button

---
# button

## Summary

Gets the mouse button that caused an event.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/MouseEvent](/dom/MouseEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var button = event.button;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

One of the following values -

-   0 - The primary button (usually the left mouse button).
-   1 - The auxiliary button (usually the middle/wheel mouse button).
-   2 - The secondary button (usually the right mouse button).

Any value higher than 2 represents other less common buttons.

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

