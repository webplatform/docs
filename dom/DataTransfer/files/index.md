---
title: files
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
summary: 'Returns a FileList of the files being dragged, if any.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/DataTransfer/files

---
## <span>Summary</span>

Returns a FileList of the files being dragged, if any.

Property of [dom/DataTransfer](/dom/DataTransfer)[dom/DataTransfer](/dom/DataTransfer)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.files;
```

## <span>Return Value</span>

Returns an object of type ObjectObject

A live FileList sequence consisting of File objects representing the files being dragged (if any).

## <span>Examples</span>

``` js
//retrieve list of files being dragged
function getDragFiles(e) {
  var oData = e.dataTransfer;
  var fList = oData.files;
}
```

## <span>Notes</span>

This version of the API does not expose the types of the files during the drag.

## <span>Related specifications</span>

[HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation
