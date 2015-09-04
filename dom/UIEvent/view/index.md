---
title: view
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - "Needs createUIEvent example????\ndon't know why you would specify a different window to the current in creteUIEvent."
summary: "Gets the window object that an event is generated from.\n[object window]\n"
uri: dom/UIEvent/view

---
# view

## Summary

Gets the window object that an event is generated from. [object window]

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/UIEvent](/dom/UIEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var eventWindow = event.view;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

The window object on which the event occurred.

**Needs Examples**: This section should include examples.

## Usage

     Use this property to determine the window object on which the event has occurred.

## Notes

Use [initUIEvent](/dom/UIEvent/initUIEvent) to set the value of this property.

## Related specifications

Specification
:   Status
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[event.view](https://developer.mozilla.org/en-US/docs/Web/API/event.view) Article]

Portions of this content come from the Microsoft Developer Network: [[view Property](http://msdn.microsoft.com/en-us/library/ie/ff974803(v=vs.85).aspx) Article]

