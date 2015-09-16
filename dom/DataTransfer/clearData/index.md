---
title: clearData
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clearDataEX.htm'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/DataTransfer
    href: /dom/DataTransfer
standardization_status: 'W3C Candidate Recommendation'
summary: 'Removes one or more data formats (or all data) from the clipboard through the DataTransfer object or the ClipboardData object.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/DataTransfer/clearData

---
## Summary

Removes one or more data formats (or all data) from the clipboard through the DataTransfer object or the ClipboardData object.

Method of [dom/DataTransfer](/dom/DataTransfer)[dom/DataTransfer](/dom/DataTransfer)

## Syntax

``` js
 event.dataTransfer.clearData(format);
```

## Parameters

### format

 Data-type
:   String

(Optional)

The format of the data to be cleared, using one of the following values (case insensitve):

-   URL
-   Text

If *format* is omitted, all data is removed.

## Return Value

No return value

## Examples

This example uses the **clearData**, [setData](/dom/DataTransfer/setData), and [getData](/dom/DataTransfer/getData) methods with the [DataTransfer](/dom/DataTransfer) object.

``` html
<!doctype html>
<html>
 <head>
  <script>
var sImageURL, oTarget, oImage;
function initiateDrag(e) {
/*  The setData parameters tell the source object
   to transfer data as a URL and provide the path.  */
  e.dataTransfer.setData("URL", oImage.src);
}
function finishDrag(e) {
  e.dataTransfer.clearData("URL");
  oTarget.textContent = e.dataTransfer.getData("URL");
}
function initialize() {
 oImage = document.getElementById("oImage");
 oTarget = document.getElementbyId("oTarget");
 oImage.addEventListener("dragstart", initiateDrag, false);
 oTarget.addEventListener("dragenter", finishDrag, false);
}
window.addEventListener("load", initialize, false);
  </script>
 </head>
 <body>
  <p>This example demonstrates how to use the setData and getData methods of the dataTransfer object to enable the source path of the image to be dragged. Since we are clearing the data, dragging over the target will show "null" instead.</p>
  <img id="oImage" src="/workshop/graphics/black.png" width="20" height="20" alt="Black">
  <span id="oTarget">
    Drop the image here
  </span>
 </body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clearDataEX.htm)

## Notes

-   If no *format* parameter is passed, all of the data formats are cleared.
-   For drag-and-drop operations, the **clearData** method of the [DataTransfer](/dom/DataTransfer) object is used generally in source events, such as [dragstart](/dom/DragEvent/dragstart). When you override the default behavior of the target, use **clearData** in the [drop](/dom/DragEvent/drop) event. It is particularly useful for selectively removing data formats when multiple formats are specified.
-   The clearData() method does not affect whether any files were included in the drag, so the types attribute's list might still not be empty after calling clearData() (it would still contain the "Files" string if any files were included in the drag).

## Related specifications

[HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation
