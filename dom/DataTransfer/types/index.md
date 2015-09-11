---
title: types
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
  - API
  - Object
  - Properties
  - DOM
uri: dom/DataTransfer/types

---
## <span>Summary</span>

Returns an array listing the formats that were set in the dragstart event. If any files are being dragged, one of the types will be the string &quot;Files&quot;.

Property of [dom/DataTransfer](/dom/DataTransfer)[dom/DataTransfer](/dom/DataTransfer)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var dragTypes = event.dataTransfer.types;
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

An array of dragged formats.

## <span>Examples</span>

``` js
//retrieve array of formats being dragged
function getDragTypes(e) {
  var oData = e.dataTransfer;
  var dTypes = oData.types;
}
```

## <span>Related specifications</span>

[HTML](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation
