{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Gets which kinds of data transfer operations are allowed for the object. Can be set (during the dragstart event) to change the allowed operations.}}
{{API_Object_Property
|Property_applies_to=dom/DataTransfer
|Read_only=No
|Example_object_name=event.dataTransfer
|Return_value_name=effectAllowed
|Javascript_data_type=String
|Return_value_description=One of the following values:
*none
*copy
*copyLink
*copyMove
*link
*linkMove
*move
*all
*uninitialized
|Example_value_name=newEffectAllowed
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the [[dom/DataTransfer/dropEffect|'''dropEffect''']] and '''effectAllowed''' properties of the [[dom/DataTransfer|'''DataTransfer''']] object to display the move cursor.
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/effectAllowedEX.htm
}}
}}
{{Notes_Section
|Notes=Set the '''effectAllowed''' property in the [[dom/DragEvent/dragstart|'''ondragstart''']] event. This property is used most effectively with the [[dom/DataTransfer/dropEffect|'''dropEffect''']] property.

This property can be used to override the default behavior in other applications. For example, the script can set the '''effectAllowed''' property to '''copy''' for a text field and override the Microsoft Word default of '''move'''. In the application, '''copy''' is the default '''effectAllowed''' behavior; however,  anchors are set to '''link''' by default, and text fields are set to '''move''' by default.

By setting '''effectAllowed''' to '''none''', dropping is disabled but the no-drop cursor is still displayed. To avoid displaying the no-drop cursor, cancel the [[dom/BeforeUnloadEvent/returnValue|'''returnValue''']] of the [[dom/DragEvent/dragstart|'''ondragstart''']] window.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML
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