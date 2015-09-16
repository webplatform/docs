---
title: 'items'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/DataTransfer
    href: /dom/DataTransfer
  return:
    predicate: 'Returns an object of type '
    value: Object
    href: /dom/DataTransfer
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns a DataTransferItemList object containing the drag data.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/DataTransfer/items

---
## Summary

Returns a DataTransferItemList object containing the drag data.

Property of [dom/DataTransfer](/dom/DataTransfer)[dom/DataTransfer](/dom/DataTransfer)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.items;
```

## Return Value

Returns an object of type ObjectObject

A DataTransferItemList object; see the [W3C specification](http://www.w3.org/TR/html5/editing.html#datatransferitemlist) for more information.

## Examples

``` js
//get DataTransfer item list
function getItemList(e) {
  var oData = e.dataTransfer;
  var iList = oData.items;
}
```

## Related specifications

[HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation
