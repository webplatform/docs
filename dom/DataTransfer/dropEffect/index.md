{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Gets the type of drag-and-drop operation currently selected or sets the operation to a new type.}}
{{API_Object_Property
|Property_applies_to=dom/DataTransfer
|Read_only=No
|Example_object_name=event.dataTransfer
|Return_value_name=dropEffect
|Javascript_data_type=String
|Return_value_description=One of the following values:
*none
*copy
*link
*move
|Example_value_name=newDropEffect
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''dropEffect''' and [[dom/DataTransfer/effectAllowed|effectAllowed]] properties of the [[dom/DataTransfer|DataTransfer]] object to display the move cursor.
|Code=<!doctype html>
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
  <h1>Example of the effectAllowed and dropEffect Properties</h1>
  <p>The code in this example sets the <b>effectAllowed</b> property 
to <span class="literal">move</span>. It sets the <b>dropEffect</b> 
property to display the move cursor. The default action must be canceled in all events that are handled&amp;#151;in this example, 
<b>ondragstart</b>, <b>ondragover</b>, <b>ondragenter</b>, and 
<b>ondrop</b>.</p>
<p>
<b>
  [not this text]
<span id="oSource">
  [select and drag this text]
</span>
  [not this text]
</b>
</p>
<p>&nbsp;</p>
<div id="oTarget">
[drop text here]
  </div>
 </body>
</html>
}}
}}
{{Notes_Section
|Notes=The '''dropEffect''' property must be used with the [[dom/DataTransfer/effectAllowed|'''effectAllowed''']] property. These properties are set on the source object of a drag-and-drop operation. The '''effectAllowed''' property determines which drag-and-drop operations are available from the source object. The '''dropEffect''' property determines which drag-and-drop operations are allowed on the target object. For example, the source object might set the '''effectAllowed''' property to '''all''' drag-and-drop operations, while the target object specifies that the '''dropEffect''' allows only '''copy''' operations.

The recommended technique for dropping text is to set the '''dropEffect''' in the target object's event handler function for the following events: [[dom/DragEvent/dragenter|'''ondragenter''']], [[dom/DragEvent/dragover|'''ondragover''']], and [[dom/DragEvent/drop|'''ondrop''']]. The [[dom/DataTransfer/effectAllowed|'''effectAllowed''']] property must be set in one of the source object's drag-and-drop event handlers, such as the [[dom/DragEvent/dragstart|'''ondragstart''']] event.

The target object of a drag-and-drop operation can set the '''dropEffect''' during the following events: [[dom/DragEvent/dragenter|'''ondragenter''']], [[dom/DragEvent/dragover|'''ondragover''']], and [[dom/DragEvent/drop|'''ondrop''']]. To display the cursor until the final drop, the default action of the following events must be canceled: '''ondragenter''', '''ondragover''', and '''ondrop''': and the '''dropEffect''' must be set. Otherwise, the copy cursor, move cursor, or link cursor set by this property displays only until the first valid drop target is intersected, at which point the cursor is replaced by the drop/no-drop cursor for the rest of the drag operation.

There is a default drag-and-drop functionality for the following elements: [[html/elements/a|'''a''']], [[html/elements/img|'''img''']], [[html/elements/textarea|'''textarea''']], and [[html/elements/input|'''input type{{=}}text''']]. When one of these objects is the source element, the default drop effect cannot be overridden by setting the '''dropEffect''' property of the target element. Instead, the default behavior of the source object must be canceled.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/editing.html
|Status=Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}