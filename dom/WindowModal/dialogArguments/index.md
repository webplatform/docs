---
title: dialogArguments
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
summary: 'Gets the arguments that are specified when showModalDialog is called.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/dialogArgumentsCallerEX1.htm'
uri: dom/WindowModal/dialogArguments

---
# dialogArguments

## Summary

Gets the arguments that are specified when showModalDialog is called.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/WindowModal](/dom/WindowModal)</span></span>

## Syntax

``` {.js}
var arguments = window.dialogArguments;
window.dialogArguments = value;
```

## Examples

The following example shows how to get information passed into a modal dialog window by using the **dialogArguments** property. The code corresponds to two different files. One file launches the modal window and the other file stores the code for the modal window.

This file launches the modal window and then sends an object to that modal window.

``` {.html}
<!doctype html>
<html>
 <head>
  <script>
function fnLaunch() {
    var aForm;
    aForm = document.getElementById("oForm").elements;
    var myObject = {};
    myObject.firstName = aForm.oFirstName.value;
    myObject.lastName = aForm.oLastName.value;
    // The object "myObject" is sent to the modal window.
    window.showModalDialog("modalDialogSource.htm", myObject, "dialogHeight:300px; dialogLeft:200px;");
}
  </script>
 </head>
 <body>
  <button onclick="fnLaunch();">Launch The Dialog</button>
  <form id= "oForm">
   First Name:
   <input type="text" name="oFirstName" value="Jane">
   <br/>
   Last Name:
   <input type="text" name="oLastName" value="Smith">
  </form>
 </body>
</html>
```

This file (modalDialogSource.htm), stores the code for the modal window. Get the object sent to this modal window by using the **dialogArguments** property.

``` {.html}
<!doctype html>
<html>
 <head>
  <script>
var oMyObject = window.dialogArguments;
var sFirstName = oMyObject.firstName;
var sLastName = oMyObject.lastName;
  </script>
  <title>Untitled</title>
 </head>
 <body style="font-family: arial; font-size: 14pt; color: Snow;
background-color: RosyBrown;">
  First Name:
  <span style="color:#00ff7f">
   <script>
document.write(sFirstName);
   </script>
  </span>
  <br/>
  Last Name:
  <span style="color:#00ff7f">
   <script>
document.write(sLastName);
   </script>
  </span>
 </body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/dialogArgumentsCallerEX1.htm)

## Notes

This property applies only to windows that are created with the [**showModalDialog**](/dom/Window/showModalDialog) method.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[dialogArguments](https://developer.mozilla.org/en-US/docs/Web/API/Window.dialogArguments) Article]

Portions of this content come from the Microsoft Developer Network: [[dialogArguments Property](http://msdn.microsoft.com/en-us/library/ie/ms533723(v=vs.85).aspx) Article]

