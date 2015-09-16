---
title: 'wasClean'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
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
    value: Boolean
    href: /dom/CloseEvent
summary: 'Indicates whether the server connection closed cleanly.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/CloseEvent/wasClean

---
## Summary

Indicates whether the server connection closed cleanly.

Property of [dom/CloseEvent](/dom/CloseEvent)[dom/CloseEvent](/dom/CloseEvent)

## Syntax

**Note**: This property is read-only.

``` js
var wasClean = event.wasClean;
```

## Return Value

Returns an object of type BooleanBoolean

Whether the connection was cleanly closed.

## Examples

``` js
function getCloseClean(e) {
//retrieve whether connection was cleanly closed
var closeClean = e.wasClean;
return closeClean;
}
```

