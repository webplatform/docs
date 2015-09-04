---
title: dropEffect
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Gets the type of drag-and-drop operation currently selected or sets the operation to a new type.'
uri: dom/DataTransfer/dropEffect

---
# dropEffect

## Summary

Gets the type of drag-and-drop operation currently selected or sets the operation to a new type.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/DataTransfer](/dom/DataTransfer)</span></span>

## Syntax

``` {.js}
var dropEffect = event.dataTransfer.dropEffect;
event.dataTransfer.dropEffect = newDropEffect;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

One of the following values:

-   none
-   copy
-   link
-   move

## Examples

This example uses the **dropEffect** and [effectAllowed](/dom/DataTransfer/effectAllowed) properties of the [DataTransfer](/dom/DataTransfer) object to display the move cursor.

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

## Notes

The **dropEffect** property must be used with the [**effectAllowed**](/dom/DataTransfer/effectAllowed) property. These properties are set on the source object of a drag-and-drop operation. The **effectAllowed** property determines which drag-and-drop operations are available from the source object. The **dropEffect** property determines which drag-and-drop operations are allowed on the target object. For example, the source object might set the **effectAllowed** property to **all** drag-and-drop operations, while the target object specifies that the **dropEffect** allows only **copy** operations.

The recommended technique for dropping text is to set the **dropEffect** in the target object's event handler function for the following events: [**ondragenter**](/dom/DragEvent/dragenter), [**ondragover**](/dom/DragEvent/dragover), and [**ondrop**](/dom/DragEvent/drop). The [**effectAllowed**](/dom/DataTransfer/effectAllowed) property must be set in one of the source object's drag-and-drop event handlers, such as the [**ondragstart**](/dom/DragEvent/dragstart) event.

The target object of a drag-and-drop operation can set the **dropEffect** during the following events: [**ondragenter**](/dom/DragEvent/dragenter), [**ondragover**](/dom/DragEvent/dragover), and [**ondrop**](/dom/DragEvent/drop). To display the cursor until the final drop, the default action of the following events must be canceled: **ondragenter**, **ondragover**, and **ondrop**: and the **dropEffect** must be set. Otherwise, the copy cursor, move cursor, or link cursor set by this property displays only until the first valid drop target is intersected, at which point the cursor is replaced by the drop/no-drop cursor for the rest of the drag operation.

There is a default drag-and-drop functionality for the following elements: [**a**](/html/elements/a), [**img**](/html/elements/img), [**textarea**](/html/elements/textarea), and [**input type=text**](/html/elements/input). When one of these objects is the source element, the default drop effect cannot be overridden by setting the **dropEffect** property of the target element. Instead, the default behavior of the source object must be canceled.

## Related specifications

Specification
:   Status
[HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

