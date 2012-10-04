{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''dropEffect''' and [[dom/properties/effectAllowed|'''effectAllowed''']] properties of the [[dom/objects/dataTransfer|'''dataTransfer''']] object to display the move cursor.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/effectAllowedEX.htm
|Code=
&lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN"&gt;
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;TITLE&gt;Example of the effectAllowed and dropEffect Properties&lt;/TITLE&gt;

&lt;SCRIPT&gt;
// This function is called when the user 
//  initiates a drag-and-drop operation.
function fnHandleDragStart()
{                                      
  var oData {{=}} window.event.dataTransfer;

  // Set the effectAllowed on the source object.
  oData.effectAllowed {{=}} "move";
}

// This function is called by the target 
//  object in the ondrop event.
function fnHandleDrop()
{
  var oTarg {{=}} window.event.srcElement;
  var oData {{=}} window.event.dataTransfer;

  // Cancel default action.
  fnCancelDefault();

  // Set the content of the oTarget to the information stored
  //  in the data transfer object in the desired format.
  oTarg.innerText +{{=}} oData.getData("text");
}

// This function sets the dropEffect when the user moves the 
//  mouse over the target object.
function fnHandleDragEnter()
{
  var oData {{=}} window.event.dataTransfer;

  // Cancel default action.
  fnCancelDefault();

  // Set the dropEffect for the target object.
  oData.dropEffect {{=}} "move";
}

function fnCancelDefault()
{
  // Cancel default action.
  var oEvent {{=}} window.event;
  oEvent.returnValue {{=}} false;
}
&lt;/SCRIPT&gt;

&lt;/HEAD&gt;

&lt;BODY&gt;
&lt;H1&gt;Example of the effectAllowed and dropEffect Properties&lt;/H1&gt;

&lt;P&gt;The code in this example sets the &lt;B&gt;effectAllowed&lt;/B&gt; property 
to &lt;SPAN CLASS{{=}}"literal"&gt;move&lt;/SPAN&gt;. It sets the &lt;B&gt;dropEffect&lt;/B&gt; 
property to display the move cursor. The default action must be 
canceled in all events that are handled&amp;#151;in this example, 
&lt;B&gt;ondragstart&lt;/B&gt;, &lt;B&gt;ondragover&lt;/B&gt;, &lt;B&gt;ondragenter&lt;/B&gt;, and 
&lt;B&gt;ondrop&lt;/B&gt;.&lt;/P&gt;
&lt;B&gt;
  [not this text]
&lt;SPAN ID{{=}}"oSource" ondragstart{{=}}"fnHandleDragStart()"&gt;
  [select and drag this text]
&lt;/SPAN&gt;
  [not this text]
&lt;/B&gt;
&lt;P&gt;&lt;BR&gt;&lt;P&gt;
&lt;DIV ID{{=}}"oTarget" 
     STYLE{{=}}"background:beige; 
            height:100;
            width:200;
            border:solid black 1px;"
     ondrop{{=}}"fnHandleDrop()"
     ondragover{{=}}"fnCancelDefault()"
     ondragenter{{=}}"fnHandleDragEnter()"&gt;
[drop text here]
&lt;/DIV&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''dropEffect''' property must be used with the [[dom/properties/effectAllowed|'''effectAllowed''']] property. These properties are set on the source object of a drag-and-drop operation. The '''effectAllowed''' property determines which drag-and-drop operations are available from the source object. The '''dropEffect''' property determines which drag-and-drop operations are allowed on the target object. For example, the source object might set the '''effectAllowed''' property to '''all''' drag-and-drop operations, while the target object specifies that the '''dropEffect''' allows only '''copy''' operations.
The recommended technique for dropping text is to set the '''dropEffect''' in the target object's event handler function for the following events: [[dom/events/dragenter|'''ondragenter''']], [[dom/events/dragover|'''ondragover''']], and [[dom/events/drop|'''ondrop''']]. The [[dom/properties/effectAllowed|'''effectAllowed''']] property must be set in one of the source object's drag-and-drop event handlers, such as the [[dom/events/dragstart|'''ondragstart''']] event.
The target object of a drag-and-drop operation can set the '''dropEffect''' during the following events: [[dom/events/dragenter|'''ondragenter''']], [[dom/events/dragover|'''ondragover''']], and [[dom/events/drop|'''ondrop''']]. To display the cursor until the final drop, the default action of the following events must be canceled: '''ondragenter''', '''ondragover''', and '''ondrop''': and the '''dropEffect''' must be set. Otherwise, the copy cursor, move cursor, or link cursor set by this property displays only until the first valid drop target is intersected, at which point the cursor is replaced by the drop/no-drop cursor for the rest of the drag operation.
Windows Internet Explorer delivers default drag-and-drop functionality for the following objects: [[html/elements/a|'''a''']], '''img''', '''textArea''', and '''input type{{=}}text'''. When one of these objects is the source element, the default drop effect cannot be overridden by setting the '''dropEffect''' property of the target element. Instead, the default behavior of the source object must be canceled.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/objects/dataTransfer|dataTransfer]]</code>
*<code>Reference</code>
*<code>[[dom/methods/clearData|clearData]]</code>
*<code>[[dom/properties/effectAllowed|effectAllowed]]</code>
*<code>[[dom/methods/getData|getData]]</code>
*<code>[[dom/methods/setData|setData]]</code>
*<code>Conceptual</code>
*<code>About DHTML Data Transfer</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}