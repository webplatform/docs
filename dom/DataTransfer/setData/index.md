---
title: setData
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Adds data in a specified format to the DataTransfer object or the ClipboardData object.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setDataEX.htm'
uri: dom/DataTransfer/setData

---
# setData

## Summary

Adds data in a specified format to the DataTransfer object or the ClipboardData object.

*Method of [dom/DataTransfer](/dom/DataTransfer)*

## Syntax

``` {.js}
 event.dataTransfer.setData(format, data);
```

## Parameters

### format

 Data-typeÂ
:   String

 The format of the data to be transferred, using one of the following values (case insensitve):

-   URL
-   Text

### data

 Data-typeÂ
:   String

 Specifies the data supplied by the source object. This information can be descriptive text, a source path to an image, or a URL for an anchor. When you pass "URL" as the *format* parameter, you must use the *data* parameter to provide the location of the object that is transferred.

## Return Value

No return value

## Examples

This example uses the **setData** method and the [**getData**](/dom/DataTransfer/getData) method with the [**DataTransfer**](/dom/DataTransfer) object to create a shortcut to an image.

``` {.html}
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
/*  The parameter passed to getData tells the target
    object what data format to expect.  */
  sImageURL = e.dataTransfer.getData("URL");
  oTarget.textContent = sImageURL;
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
  <p>This example demonstrates how to use the setData and getData methods of the dataTransfer object to enable the source path of the image to be dragged.</p>
  <img id="oImage" src="/workshop/graphics/black.png" width="20" height="20" alt="Black">
  <span id="oTarget">
    Drop the image here
  </span>
 </body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setDataEX.htm)

## Related specifications

Specification
:   Status
[HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

