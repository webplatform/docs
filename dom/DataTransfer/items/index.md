---
title: items
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns a DataTransferItemList object containing the drag data.'
uri: dom/DataTransfer/items

---
# items

## Summary

Returns a DataTransferItemList object containing the drag data.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/DataTransfer](/dom/DataTransfer)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.items;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

A DataTransferItemList object; see the [W3C specification](http://www.w3.org/TR/html5/editing.html#datatransferitemlist) for more information.

## Examples

``` {.js}
//get DataTransfer item list
function getItemList(e) {
  var oData = e.dataTransfer;
  var iList = oData.items;
}
```

## Related specifications

Specification
:   Status
[HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation

