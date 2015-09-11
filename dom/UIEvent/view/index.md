---
title: view
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[event.view](https://developer.mozilla.org/en-US/docs/Web/API/event.view) Article]'
  - 'Microsoft Developer Network: [[view Property](http://msdn.microsoft.com/en-us/library/ie/ff974803(v=vs.85).aspx) Article]'
notes:
  - "Needs createUIEvent example????\ndon't know why you would specify a different window to the current in creteUIEvent."
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/UIEvent
    href: /dom/UIEvent
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/UIEvent
standardization_status: 'W3C Working Draft'
summary: "Gets the window object that an event is generated from.\n[object window]\n"
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/UIEvent/view

---
## <span>Summary</span>

Gets the window object that an event is generated from. [object window]

Property of [dom/UIEvent](/dom/UIEvent)[dom/UIEvent](/dom/UIEvent)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var eventWindow = event.view;
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The window object on which the event occurred.

**Needs Examples**: This section should include examples.

## <span>Usage</span>

     Use this property to determine the window object on which the event has occurred.

## <span>Notes</span>

Use [initUIEvent](/dom/UIEvent/initUIEvent) to set the value of this property.

## <span>Related specifications</span>

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
