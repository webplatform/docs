---
title: effectAllowed
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Gets which kinds of data transfer operations are allowed for the object. Can be set (during the dragstart event) to change the allowed operations.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/effectAllowedEX.htm'
uri: dom/DataTransfer/effectAllowed

---
# effectAllowed

## Summary

Gets which kinds of data transfer operations are allowed for the object. Can be set (during the dragstart event) to change the allowed operations.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/DataTransfer](/dom/DataTransfer)</span></span>

## Syntax

``` {.js}
var effectAllowed = event.dataTransfer.effectAllowed;
event.dataTransfer.effectAllowed = newEffectAllowed;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

One of the following values:

-   none
-   copy
-   copyLink
-   copyMove
-   link
-   linkMove
-   move
-   all
-   uninitialized

## Examples

This example uses the [**dropEffect**](/dom/DataTransfer/dropEffect) and **effectAllowed** properties of the [**DataTransfer**](/dom/DataTransfer) object to display the move cursor.

``` {.html}
<!doctype html>
<html>
 <head>
  <title>Example of the effectAllowed and dropEffect Properties</title>
  <style>
#oTarget {
  background: beige;
  height: 100px;
  width: 200px;
  border: solid black 1px;
}
  </style>
  <script>
// This function is called when the user
// initiates a drag-and-drop operation.
function fnHandleDragStart(e) {
  var oData = e.dataTransfer;
  // Set the effectAllowed on the source object.
  oData.effectAllowed = "move";
}

// This function is called by the target
// object in the ondrop event.
function fnHandleDrop(e) {
  var oTarg = e.target;
  var oData = e.dataTransfer;

  // Cancel default action.
  fnCancelDefault(e);

  // Set the content of the oTarget to the information stored
  // in the data transfer object in the desired format.
  oTarg.textContent += oData.getData("Text");
}

// This function sets the dropEffect when the user moves the
// mouse over the target object.
function fnHandleDragEnter(e) {
  var oData = e.dataTransfer;

  // Cancel default action.
  fnCancelDefault(e);

  // Set the dropEffect for the target object.
  oData.dropEffect = "move";
}

function fnCancelDefault(e) {
  // Cancel default action.
  e.preventDefault();
}
function initialize() {
 var target = document.getElementById("oTarget");
 document.getElementById("oSource").addEventListener("dragstart", fnHandleDragStart, false);
 target.addEventListener("drop", fnHandleDrop, false);
 target.addEventListener("ondragover", fnCancelDefault, false);
 target.addEventListener("ondragenter", fnHandleDragEnter, false);
}

window.addEventListener("load", initialize, false);
  </script>
 </head>
 <body>
  Example of the effectAllowed and dropEffect Properties
  The code in this example sets the effectAllowed property
to move. It sets the dropEffect
property to display the move cursor. The default action must be canceled in all events that are handled&#151;in this example,
ondragstart, ondragover, ondragenter, and
ondrop.


  [not this text]

  [select and drag this text]

  [not this text]


Â

[drop text here]


</body>
```

\</html\>

</pre>
[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/effectAllowedEX.htm)

## Notes

Set the **effectAllowed** property in the [**ondragstart**](/dom/DragEvent/dragstart) event. This property is used most effectively with the [**dropEffect**](/dom/DataTransfer/dropEffect) property.

This property can be used to override the default behavior in other applications. For example, the script can set the **effectAllowed** property to **copy** for a text field and override the Microsoft Word default of **move**. In the application, **copy** is the default **effectAllowed** behavior; however, anchors are set to **link** by default, and text fields are set to **move** by default.

By setting **effectAllowed** to **none**, dropping is disabled but the no-drop cursor is still displayed. To avoid displaying the no-drop cursor, cancel the [**returnValue**](/dom/BeforeUnloadEvent/returnValue) of the [**ondragstart**](/dom/DragEvent/dragstart) window.

## Related specifications

Specification
:   Status
[HTML](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

