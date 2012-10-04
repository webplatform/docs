{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=offset|Data type=Integer|Description=A '''Integer''' that specifies the index of the string that indicates where the separation occurs. If a value is not provided, a new text node with no value is created.|Optional=}}
|Method_applies_to=dom/TextNode
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLDOMNode'''

Returns a text node object.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''splitText''' method to divide a text node in half in a '''ul''' object. When the text node splits, the [[dom/methods/createElement|'''createElement''']] method creates a new '''li''' object. The [[dom/methods/appendChild|'''appendChild''']] method appends the new '''li''' element and the split text node to the '''ul''' object.
|LiveURL=
|Code=
&lt;SCRIPT&gt;
function fnSplitNode(){
   var oNode{{=}}oList.firstChild.childNodes(0);
   var oNewNode{{=}}document.createElement("LI");
   var oSplitNode {{=}} oNode.splitText(oNode.nodeValue.length/2);
   oList.appendChild(oNewNode);
   oNewNode.appendChild(oSplitNode);
}
&lt;/SCRIPT&gt;
&lt;UL onclick{{=}}"fnSplitNode()" id{{=}}"oList"&gt;
&lt;LI&gt;This is a list item.
&lt;/UL&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The text node that invokes the '''splitText''' method has a [[dom/properties/nodeValue|'''nodeValue''']] equal to the substring of the value, from zero to ''offset''. The new text node has a '''nodeValue''' of the substring of the original value, from the specified index to the value length. Text node integrity is not preserved when the document is saved or persisted.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/TextNode|TextNode]]</code>
*<code>[[dom/methods/createElement|createElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}