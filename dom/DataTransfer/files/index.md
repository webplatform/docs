---
title: 'files'
compatibility:
  feature: files
  topic: dom
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
  - API_Object_Properties
  - DOM
uri: dom/DataTransfer/files

---
## Summary

Returns a FileList of the files being dragged, if any.

Property of [dom/DataTransfer](/dom/DataTransfer)[dom/DataTransfer](/dom/DataTransfer)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.files;
```

## Return Value

Returns an object of type ObjectObject

A live FileList sequence consisting of File objects representing the files being dragged (if any).

## Examples

``` js
//retrieve list of files being dragged
function getDragFiles(e) {
  var oData = e.dataTransfer;
  var fList = oData.files;
}
```

## Notes

This version of the API does not expose the types of the files during the drag.

## Related specifications

[HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation
