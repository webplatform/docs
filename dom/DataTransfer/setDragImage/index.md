---
title: 'setDragImage'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/DataTransfer
    href: /dom/DataTransfer
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /dom/DataTransfer
standardization_status: 'W3C Candidate Recommendation'
summary: 'Uses the given element to update the drag feedback image, replacing any previously specified feedback image.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/DataTransfer/setDragImage

---
## Summary

Uses the given element to update the drag feedback image, replacing any previously specified feedback image.

Method of [dom/DataTransfer](/dom/DataTransfer)[dom/DataTransfer](/dom/DataTransfer)

## Syntax

``` js
var result = element.setDragImage(element, x, y);
```

## Parameters

### element

 Data-type
:   Object

 An "img" element, used to set the drag data store bitmap to the element's image (at its intrinsic size). If not an "img" element, used to set the drag data store bitmap to an image generated from the given element, although the mechanism for doing so is not currently specified.

### x

 Data-type
:   unsigned long

 The "x" value of the drag data store hot spot coordinate.

### y

 Data-type
:   unsigned long

 The "y" value of the drag data store hot spot coordinate.

## Return Value

Returns an object of type

## Examples

``` js
//set new drag feedback image
function setDragImage(e) {
  var img = document.getElementById("dragimg");
  var oData = e.dataTransfer;
  oData.setDragImage (img, 0, 0);
}
```

## Related specifications

[HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation
