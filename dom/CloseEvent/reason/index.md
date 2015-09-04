---
title: reason
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'The connection close text provided by the server.'
uri: dom/CloseEvent/reason

---
# reason

## Summary

The connection close text provided by the server.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/CloseEvent](/dom/CloseEvent)</span></span>

## Syntax

``` {.js}
var result = element.reason;
element.reason = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The connection close text provided by the server.

## Examples

``` {.js}
function getCloseReason(e) {
//retrieve close text for closeEvent
var closeReason = e.reason;
return closeReason;
}
```

