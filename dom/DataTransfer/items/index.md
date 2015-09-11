---
title: items
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
## <span>Summary</span>

Returns a DataTransferItemList object containing the drag data.

Property of [dom/DataTransfer](/dom/DataTransfer)[dom/DataTransfer](/dom/DataTransfer)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.items;
```

## <span>Return Value</span>

Returns an object of type ObjectObject

A DataTransferItemList object; see the [W3C specification](http://www.w3.org/TR/html5/editing.html#datatransferitemlist) for more information.

## <span>Examples</span>

``` js
//get DataTransfer item list
function getItemList(e) {
  var oData = e.dataTransfer;
  var iList = oData.items;
}
```

## <span>Related specifications</span>

[HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation
