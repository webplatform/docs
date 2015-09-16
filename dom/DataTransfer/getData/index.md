---
title: getData
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setDataEX.htm'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/DataTransfer
    href: /dom/DataTransfer
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /dom/DataTransfer
standardization_status: 'W3C Candidate Recommendation'
summary: "Gets the data in the specified format from the clipboard through the DataTransfer object or the ClipboardData object.\nIf there is no data, returns an empty string.\n"
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/DataTransfer/getData

---
## Summary

Gets the data in the specified format from the clipboard through the DataTransfer object or the ClipboardData object. If there is no data, returns an empty string.

Method of [dom/DataTransfer](/dom/DataTransfer)[dom/DataTransfer](/dom/DataTransfer)

## Syntax

``` js
var eventData = event.dataTransfer.getData(format);
```

## Parameters

### format

 Data-type
:   String

 The format of the data to be transferred, using one of the following values (case insensitve):

-   URL
-   Text

## Return Value

Returns an object of type StringString

Returns the data in the format retrieved from the clipboard/drag and drop operation through the [**DataTransfer**](/dom/DataTransfer) object or the [**ClipboardData**](/dom/ClipboardData) object. Depending on the information contained in [**setData**](/dom/DataTransfer/setData), this variable can get a path to an image, text, or an anchor URL.

## Examples

This example uses the **getData** method and the [**setData**](/dom/DataTransfer/setData) method with the [**DataTransfer**](/dom/DataTransfer) object to create a shortcut to an image.

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

## Notes

-   The **getData** method enforces cross-frame security and allows data transfers only in the same domain. To the user, this means that a selection that is dragged between different security protocols, such as HTTP and HTTPS, fails. In addition, that a selection that is dragged between two instances of the application with different security levels, where the first instance is set to medium and the second is set to high, fails. Finally, that a selection that is dragged into the application from another drag-enabled application, such as Microsoft Word, also fails.
-   To use the **getData** method to get data from the clipboard in the **oncopy** event or the **oncut** event, you must call [event.preventDefault()](/dom/Event/preventDefault) in the event handler script.

## Related specifications

[HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation
