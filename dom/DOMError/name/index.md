---
title: name
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs spec reference'
summary: 'Returns the name of an error that occurred during a DOM operation.'
uri: dom/DOMError/name

---
# name

## Summary

Returns the name of an error that occurred during a DOM operation.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/DOMError](/dom/DOMError)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var errorName = error.name;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The name associated with an error.

## Examples

``` {.js}
function getErrorName(e) {
//retrieve name text for DOMError
var errorName = e.name;
return errorName;
}
```

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

