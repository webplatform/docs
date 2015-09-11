---
title: dialogHeight
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/dialogHeight.htm'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/WindowModal
    href: /dom/WindowModal
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/WindowModal
summary: 'Gets or sets the height of the content area of a dialog window.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/WindowModal/dialogHeight

---
## <span>Summary</span>

Gets or sets the height of the content area of a dialog window.

Property of [dom/WindowModal](/dom/WindowModal)[dom/WindowModal](/dom/WindowModal)

## <span>Syntax</span>

``` js
var height = window.dialogHeight;
window.dialogHeight = newHeight;
```

## <span>Return Value</span>

Returns an object of type StringString

The height of the content area of the dialog window and a unit of measure.

## <span>Examples</span>

This example creates a dialog window using the **dialogHeight** property to set the new window's height.

``` html
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

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/dialogHeight.htm)

## <span>Notes</span>

-   This property applies only to windows that are created by using the [**showModalDialog**](/dom/Window/showModalDialog) method.
-   When a script calls the **showModalDialog** method, it suspends execution until the modal dialog box is closed. As a result, the script cannot use the **dialogHeight** property to change the appearance of the modal dialog box. To control the appearance of the modal dialog box, use script in the file loaded by the **sURL** parameter or use the value of the **sFeatures** parameter to specify the desired settings.
-   Although a user can manually adjust the height of a dialog box to a smaller value—provided the dialog box is resizable—the minimum **dialogHeight** you can set using script is 100 pixels.
-   The default unit of measure is `px`.
-   The value can be an integer or floating-point number, followed by an absolute units designator (`cm`, `mm`, `in`, `pt`, or `pc`), or a relative units designator (`em`, `ex`, or `px`).
-   For consistent results, specify this property and [**dialogWidth**](/dom/WindowModal/dialogWidth) in pixels when you design modal dialog boxes.
