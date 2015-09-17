---
title: 'types'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/DataTransfer
    href: /dom/DataTransfer
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/DataTransfer
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns an array listing the formats that were set in the dragstart event. If any files are being dragged, one of the types will be the string &quot;Files&quot;.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/DataTransfer/types

---
## Summary

Returns an array listing the formats that were set in the dragstart event. If any files are being dragged, one of the types will be the string &quot;Files&quot;.

Property of [dom/DataTransfer](/dom/DataTransfer)[dom/DataTransfer](/dom/DataTransfer)

## Syntax

**Note**: This property is read-only.

``` js
var dragTypes = event.dataTransfer.types;
```

## Return Value

Returns an object of type DOM NodeDOM Node

An array of dragged formats.

## Examples

``` js
//retrieve array of formats being dragged
function getDragTypes(e) {
  var oData = e.dataTransfer;
  var dTypes = oData.types;
}
```

## Related specifications

[HTML](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation
