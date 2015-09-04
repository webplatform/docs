---
title: types
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns an array listing the formats that were set in the dragstart event. If any files are being dragged, one of the types will be the string "Files".'
uri: dom/DataTransfer/types

---
# types

## Summary

Returns an array listing the formats that were set in the dragstart event. If any files are being dragged, one of the types will be the string "Files".

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/DataTransfer](/dom/DataTransfer)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var dragTypes = event.dataTransfer.types;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

An array of dragged formats.

## Examples

``` {.js}
//retrieve array of formats being dragged
function getDragTypes(e) {
  var oData = e.dataTransfer;
  var dTypes = oData.types;
}
```

## Related specifications

Specification
:   Status
[HTML](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

