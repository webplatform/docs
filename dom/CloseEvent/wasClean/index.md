---
title: wasClean
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'Indicates whether the server connection closed cleanly.'
uri: dom/CloseEvent/wasClean

---
# wasClean

## Summary

Indicates whether the server connection closed cleanly.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/CloseEvent](/dom/CloseEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var wasClean = event.wasClean;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Whether the connection was cleanly closed.

## Examples

``` {.js}
function getCloseClean(e) {
//retrieve whether connection was cleanly closed
var closeClean = e.wasClean;
return closeClean;
}
```

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

