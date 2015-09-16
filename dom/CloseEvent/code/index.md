---
title: code
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
    value: Number
    href: /dom/CloseEvent
summary: 'The connection close code provided by the server.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/CloseEvent/code

---
## Summary

The connection close code provided by the server.

Property of [dom/CloseEvent](/dom/CloseEvent)[dom/CloseEvent](/dom/CloseEvent)

## Syntax

**Note**: This property is read-only.

``` js
var closeCode = event.code;
```

## Return Value

Returns an object of type NumberNumber

The close code provided by the server.

## Examples

``` js
function getCloseCode(e) {
//retrieve close code for closeEvent
var closeCode = e.code;
return closeCode;
}
```

