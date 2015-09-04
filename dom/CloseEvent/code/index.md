---
title: code
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'The connection close code provided by the server.'
uri: dom/CloseEvent/code

---
# code

## Summary

The connection close code provided by the server.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/CloseEvent](/dom/CloseEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var closeCode = event.code;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

The close code provided by the server.

## Examples

``` {.js}
function getCloseCode(e) {
//retrieve close code for closeEvent
var closeCode = e.code;
return closeCode;
}
```

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

