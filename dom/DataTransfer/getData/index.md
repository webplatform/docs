{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=format|Data type=BSTR|Description=A '''String''' that specifies one of the following data format values.|Optional=}}
|Method_applies_to=dom/properties/dataTransfer
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Variant

'''Variant''' of type '''String'''. Returns the data in the format retrieved from the clipboard through the [[dom/objects/dataTransfer|'''dataTransfer''']] object or the [[dom/clipboardData|'''clipboardData''']] object. Depending on the information contained in [[dom/methods/setData|'''setData''']], this variable can get a path to an image, text, or an anchor URL.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the [[dom/methods/setData|'''setData''']] method and the '''getData''' method of the [[dom/objects/dataTransfer|'''dataTransfer''']] object to drop text in a new location and create a desktop shortcut.

This example uses the '''getData''' method to drag text and drop it in a new location.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getDataEX.htm
|Code=
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function InitiateDrag(){
  event.dataTransfer.setData(oSource.innerText);
}
function FinishDrag(){
  window.event.returnValue{{=}}false;
  oTarget.innerText {{=}} event.dataTransfer.getData("Text");
}
function OverDrag(){
  window.event.returnValue{{=}}false;
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;B ID{{=}}"oSource"
   ondragstart{{=}}"InitiateDrag()"&gt;
drag this text&lt;/B&gt;
&lt;SPAN ID{{=}}"oTarget"
   ondragover{{=}}"OverDrag()"
   ondragenter{{=}}"FinishDrag()""&gt;
drop text here&lt;/SPAN&gt;
&lt;/BODY&gt;
}}
{{Single_Example
|Description=This example uses the '''getData''' method to create a desktop shortcut using a drag-and-drop operation.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/obj_dataTransferEX.htm
|Code=
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function InitiateDrag(){   
  event.dataTransfer.setData("URL", oSource.href);
}
function FinishDrag(){
  oTarget.innerText {{=}} event.dataTransfer.getData("URL");
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;A ID{{=}}oSource HREF{{=}}"about:Example_Complete" 
   onclick{{=}}"return(false)" ondragstart{{=}}"InitiateDrag()"&gt;Test Anchor&lt;/A&gt;
&lt;SPAN ID{{=}}oTarget ondrop{{=}}"FinishDrag()"&gt;Drop Here&lt;/SPAN&gt;
&lt;/BODY&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''getData''' method enforces cross-frame security and allows data transfers only in the same domain. To the user, this means that a selection that is dragged between different security protocols, such as HTTP and HTTPS, fails. In addition, that a selection that is dragged between two instances of the application with different security levels, where the first instance is set to medium and the second is set to high, fails. Finally, that a selection that is dragged into the application from another drag-enabled application, such as Microsoft Word, also fails.
To use the '''getData''' method to get data from the clipboard in the '''oncopy''' event or the [[dom/events/cut|'''oncut''']] event, specify '''window.event.returnValue{{=}}false''' in the event handler script.
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
*<code>[[dom/methods/clearData|clearData]]</code>
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