---
title: button
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, compatibility, more info'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/MouseEvent
    href: /dom/MouseEvent
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/MouseEvent
standardization_status: 'W3C Working Draft'
summary: 'Gets the mouse button that caused an event.'
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
uri: dom/MouseEvent/button

---
## Summary

Gets the mouse button that caused an event.

Property of [dom/MouseEvent](/dom/MouseEvent)[dom/MouseEvent](/dom/MouseEvent)

## Syntax

**Note**: This property is read-only.

``` js
var button = event.button;
```

## Return Value

Returns an object of type NumberNumber

One of the following values -

-   0 - The primary button (usually the left mouse button).
-   1 - The auxiliary button (usually the middle/wheel mouse button).
-   2 - The secondary button (usually the right mouse button).

Any value higher than 2 represents other less common buttons.

**Needs Examples**: This section should include examples.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
