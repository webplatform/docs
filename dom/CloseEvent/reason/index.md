---
title: reason
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/CloseEvent
    href: /dom/CloseEvent
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/CloseEvent
summary: 'The connection close text provided by the server.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/CloseEvent/reason

---
## Summary

The connection close text provided by the server.

Property of [dom/CloseEvent](/dom/CloseEvent)[dom/CloseEvent](/dom/CloseEvent)

## Syntax

``` js
var result = element.reason;
element.reason = value;
```

## Return Value

Returns an object of type StringString

The connection close text provided by the server.

## Examples

``` js
function getCloseReason(e) {
//retrieve close text for closeEvent
var closeReason = e.reason;
return closeReason;
}
```

