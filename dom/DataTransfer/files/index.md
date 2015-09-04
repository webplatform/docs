---
title: files
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns a FileList of the files being dragged, if any.'
uri: dom/DataTransfer/files

---
# files

## Summary

Returns a FileList of the files being dragged, if any.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/DataTransfer](/dom/DataTransfer)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.files;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

A live FileList sequence consisting of File objects representing the files being dragged (if any).

## Examples

``` {.js}
//retrieve list of files being dragged
function getDragFiles(e) {
  var oData = e.dataTransfer;
  var fList = oData.files;
}
```

## Notes

This version of the API does not expose the types of the files during the drag.

## Related specifications

Specification
:   Status
[HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation

