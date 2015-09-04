---
title: dialogTop
tags:
  - API
  - Object
  - Properties
  - DOM
summary: 'Gets or sets the Y coordinate position of a dialog window.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/dialogTop.htm'
uri: dom/WindowModal/dialogTop

---
# dialogTop

## Summary

Gets or sets the Y coordinate position of a dialog window.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/WindowModal](/dom/WindowModal)</span></span>

## Syntax

``` {.js}
var yCoordinate = window.dialogTop;
window.dialogTop = newXCoordinate;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The X coordinate position and a unit of measure.

## Examples

This example creates a dialog window using the **dialogTop** property to set the position relative to the top of the screen.

``` {.html}
<!doctype html>
<html>
 <head>
  <script>
function someMessage(e) {
    e.target.blur();
    window.showModalDialog("message.htm", "",
        "dialogWidth:5cm; dialogHeight:10cm; dialogTop:0cm; dialogLeft:0cm")
}
  </script>
 </head>
 <body>
  <select onchange="someMessage(event)">
   <option>Item 1</option>
   <option>Item 2</option>
   <option>Item 3</option>
  </select>
 </body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/dialogTop.htm)

## Notes

-   This property applies only to windows that are created by using the [**showModalDialog**](/dom/Window/showModalDialog) method.
-   When a script calls the **showModalDialog** method, it suspends execution until the modal dialog box is closed. As a result, the script cannot use the **dialogTop** property to change the appearance of the modal dialog box. To control the appearance of the modal dialog box, use script in the file loaded by the **sURL** parameter or use the value of the **sFeatures** parameter to specify the desired settings.
-   The default unit of measure is `px`
-   The value can be an integer or floating-point number, followed by an absolute units designator (`cm`, `mm`, `in`, `pt`, or `pc`), or a relative units designator (`em`, `ex`, or `px`). For consistent results, specify the `dialogTop` in pixels when you design modal dialog boxes.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

