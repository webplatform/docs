{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Divides a text node at the specified index.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=offset
|Data type=String
|Description=The index of the string that indicates where the separation occurs. If a value is not provided, a new text node with no value is created.
|Optional=No
}}
|Method_applies_to=dom/Text
|Example_object_name=textNode
|Return_value_name=textNode
|Javascript_data_type=DOM Node
|Return_value_description=A text node object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''splitText''' method to divide a text node in half in a '''ul''' object. When the text node splits, the [[dom/Document/createElement|'''createElement''']] method creates a new '''li''' object. The [[dom/Node/appendChild|'''appendChild''']] method appends the new '''li''' element and the split text node to the '''ul''' object.
|Code=&lt;script&gt;
function fnSplitNode(){
   var oNode{{=}}oList.firstChild.childNodes(0);
   var oNewNode{{=}}document.createElement("LI");
   var oSplitNode {{=}} oNode.splitText(oNode.nodeValue.length/2);
   oList.appendChild(oNewNode);
   oNewNode.appendChild(oSplitNode);
}
&lt;/script&gt;
&lt;ul onclick{{=}}"fnSplitNode()" id{{=}}"oList"&gt;
&lt;li&gt;This is a list item.&lt;/li&gt;
&lt;/ul&gt;
}}
}}
{{Notes_Section
|Notes=The text node that invokes the '''splitText''' method has a [[dom/Node/nodeValue|'''nodeValue''']] equal to the substring of the value, from zero to ''offset''. The new text node has a '''nodeValue''' of the substring of the original value, from the specified index to the value length. Text node integrity is not preserved when the document is saved or persisted.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.4
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Text.splitText Text.splitText]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536764(v=vs.85).aspx splitText Method]
|HTML5Rocks_link=
}}