---
title: message
notes:
  - 'Needs spec reference'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/DOMError
    href: /dom/DOMError
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/DOMError
summary: 'Returns the message associated with an error that occurred during a DOM operation.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/DOMError/message

---
## Summary

Returns the message associated with an error that occurred during a DOM operation.

Property of [dom/DOMError](/dom/DOMError)[dom/DOMError](/dom/DOMError)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.message;
```

## Return Value

Returns an object of type StringString

The message associated with an error.

## Examples

``` js
function getErrorMsg(e) {
//retrieve message text for DOMError
var errorMsg = e.message;
return errorMsg;
}
```

