{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Creates a text node.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=text
|Data type=String
|Description=The [[dom/Node/nodeValue|'''nodeValue''']] property of the text node.
|Optional=No
}}
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=textNode
|Javascript_data_type=DOM Node
|Return_value_description=The created TextNode.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;script&gt;
function changeNode() {
   var textNode {{=}} document.createTextNode("New Text");
   var replaceNode {{=}} document.getElementById("span").childNodes(0);
   replaceNode.replaceNode(textNode);
}
&lt;/script&gt;
&lt;span id{{=}}"span" onclick{{=}}"changeNode()"&gt;
Original Text
&lt;/span&gt;
}}
}}
{{Notes_Section}}
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>[[dom/Document/createElement|createElement]]</code>
*<code>Conceptual</code>
*<code>About the W3C Document Object Model</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}