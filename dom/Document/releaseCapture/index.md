---
title: releaseCapture
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
standardization_status: Non-Standard
notes:
  - 'Needs compat tables and specs'
summary: 'Removes mouse capture from the object in the current document.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/releaseCaptureEX.htm'
uri: dom/Document/releaseCapture

---
# releaseCapture

## Summary

Removes mouse capture from the object in the current document.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
 document.releaseCapture();
```

## Return Value

No return value

## Examples

This example invokes the **releaseCapture** method on the document object.

``` {.html}
<!doctype html>
<html>
 <head>
  <title></title>
 </head>
 <body onload="oOwnCapture.setCapture();"
    onclick="document.releaseCapture();">
  <div id="oOwnCapture"
    onmousemove="oWriteLocation.value =
        event.clientX + event.clientY";
    onlosecapture="alert(event.srcElement.id +
        ' has lost mouse capture.')">
  <textarea id="oWriteLocation" cols="2"></textarea>
  </div>
  <hr/>
  <div id=oNoCapture>
   <p>Click the document to invoke the releaseCapture method.</p>
  </div>
 </body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/releaseCaptureEX.htm)

## Notes

-   For **releaseCapture** to have an effect, you must set mouse capture through the **setCapture** method.
-   You can invoke the **releaseCapture** method on the [**Document**](/dom/Document) object.
-   The **releaseCapture** method makes it unnecessary to determine which element has capture to programmatically release it.
-   Other actions that release document capture include displaying a modal dialog box and switching focus to another application or browser window.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

