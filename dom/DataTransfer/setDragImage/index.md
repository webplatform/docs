---
title: setDragImage
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Uses the given element to update the drag feedback image, replacing any previously specified feedback image.'
uri: dom/DataTransfer/setDragImage

---
# setDragImage

## Summary

Uses the given element to update the drag feedback image, replacing any previously specified feedback image.

*Method of [dom/DataTransfer](/dom/DataTransfer)*

## Syntax

``` {.js}
var result = element.setDragImage(element, x, y);
```

## Parameters

### element

 Data-typeÂ
:   Object

 An "img" element, used to set the drag data store bitmap to the element's image (at its intrinsic size). If not an "img" element, used to set the drag data store bitmap to an image generated from the given element, although the mechanism for doing so is not currently specified.

### x

 Data-typeÂ
:   unsigned long

 The "x" value of the drag data store hot spot coordinate.

### y

 Data-typeÂ
:   unsigned long

 The "y" value of the drag data store hot spot coordinate.

## Return Value

Returns an object of type .

## Examples

``` {.js}
//set new drag feedback image
function setDragImage(e) {
  var img = document.getElementById("dragimg");
  var oData = e.dataTransfer;
  oData.setDragImage (img, 0, 0);
}
```

## Related specifications

Specification
:   Status
[HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation

