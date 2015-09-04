---
title: message
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference'
summary: 'Returns the message associated with an error that occurred during a DOM operation.'
uri: dom/DOMError/message

---
# message

## Summary

Returns the message associated with an error that occurred during a DOM operation.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/DOMError](/dom/DOMError)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.message;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The message associated with an error.

## Examples

``` {.js}
function getErrorMsg(e) {
//retrieve message text for DOMError
var errorMsg = e.message;
return errorMsg;
}
```

