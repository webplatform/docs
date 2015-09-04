---
title: dialogWidth
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: readiness-state
summary: 'Gets or sets the width of the content area of a dialog window.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/dialogWidth.htm'
uri: dom/WindowModal/dialogWidth

---
# dialogWidth

## Summary

Gets or sets the width of the content area of a dialog window.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/WindowModal](/dom/WindowModal)</span></span>

## Syntax

``` {.js}
var dialogWidth = window.dialogWidth;
window.dialogWidth = newDialogWidth;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The width of the window and a unit of measure.

## Examples

This example creates a dialog window using the **dialogWidth** property to set the new window's width.

``` {.html}
<!doctype html>
<html>
 <head>
  <script>
function someMessage(e) {
    e.target.blur();
    window.showModalDialog("message.htm", "",
        "dialogWidth:5cm; dialogHeight:10cm")
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

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/dialogWidth.htm)

## Notes

-   This property applies only to windows that are created by using the [**showModalDialog**](/dom/Window/showModalDialog) method.
-   When a script calls the **showModalDialog** method, it suspends execution until the modal dialog box is closed. As a result, the script cannot use the **dialogWidth** property to change the appearance of the modal dialog box. To control the appearance of the modal dialog box, use script in the file loaded by the **sURL** parameter or use the value of the **sFeatures** parameter to specify the desired settings.
-   The default unit of measure is `px`
-   The value can be an integer or floating-point number, followed by an absolute units designator (`cm`, `mm`, `in`, `pt`, or `pc`), or a relative units designator (`em`, `ex`, or `px`). For consistent results, specify the `dialogHeight` and `dialogWidth` in pixels when you design modal dialog boxes.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

