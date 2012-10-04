{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=format|Data type=BSTR|Description=A '''String''' that specifies one or more of the following data format values.|Optional=}}
|Method_applies_to=dom/objects/StorageEvent,dom/properties/dataTransfer
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Boolean


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''clearData''' method to remove the '''Text''' data format from the clipboard through the [[dom/objects/dataTransfer|'''dataTransfer''']] object.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clearDataEX.htm
|Code=
&lt;HEAD&gt;
&lt;STYLE&gt;
DIV {background-color:magenta; width: 300;}
SPAN {color:lightgreen;}
&lt;/STYLE&gt;
&lt;SCRIPT&gt;
function Source_DragStart(){
  event.dataTransfer.setData("Text", "This text will be cleared");
}
function Target_Enter(){
  window.event.returnValue {{=}} false;
  event.dataTransfer.clearData("Text");
  oTarget.innerText {{=}} event.dataTransfer.getData("Text");
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;P&gt;Drag the green text and drop it over the magenta DIV.&lt;/P&gt;
&lt;SPAN ID{{=}}"oSource" ondragstart{{=}}"Source_DragStart()"&gt;
    Drag this text.
&lt;/SPAN&gt;
&lt;P&gt;Drop the text below. The word "null" will appear in the DIV.&lt;/P&gt;
&lt;DIV
   ID{{=}}"oTarget" ondragenter{{=}}"Target_Enter()"&gt;
&lt;/DIV&gt;
&lt;/BODY&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
If no ''format'' parameter is passed, the data formats are cleared.
For drag-and-drop operations, the '''clearData''' method of the [[dom/objects/dataTransfer|'''dataTransfer''']] object is used generally in source events, such as [[dom/events/dragstart|'''ondragstart''']]. When you override the default behavior of the target, use '''clearData''' in the [[dom/events/drop|'''ondrop''']] event. It is particularly useful for selectively removing data formats when multiple formats are specified.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/clipboardData|clipboardData]]</code>
*<code>[[dom/objects/dataTransfer|dataTransfer]]</code>
*<code>Reference</code>
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