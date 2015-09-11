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
## <span>Summary</span>

The connection close text provided by the server.

Property of [dom/CloseEvent](/dom/CloseEvent)[dom/CloseEvent](/dom/CloseEvent)

## <span>Syntax</span>

``` js
var result = element.reason;
element.reason = value;
```

## <span>Return Value</span>

Returns an object of type StringString

The connection close text provided by the server.

## <span>Examples</span>

``` js
function getCloseReason(e) {
//retrieve close text for closeEvent
var closeReason = e.reason;
return closeReason;
}
```

