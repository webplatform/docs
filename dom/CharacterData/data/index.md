{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name|data}}
{{Summary_Section|Sets or gets the value of a '''TextNode'''.}}
{{API_Object_Property
|Property_applies_to=dom/CharacterData
|Read_only=No
|Example_object_name=textualNode
|Return_value_name=text
|Javascript_data_type=String
|Return_value_description=The value of the text node.
|Example_value_name=newText
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''data''' property to change the value of a text node.
|Code=&lt;script&gt;
function fnChangeValue(){
   var oNode {{=}} oList.firstChild.childNodes(0);
   var oNewText {{=}} document.createTextNode();
   oNewText.data{{=}}"Create Data";
   oNode.replaceNode(oNewText);
   oNode.data {{=}} "New Node Value";
}
&lt;/script&gt;
&lt;ul id{{=}}"oList" onclick{{=}}"fnChangeValue()"&gt;
&lt;li&gt;Start Here&lt;/li&gt;
&lt;/ul&gt;
}}
}}
{{Notes_Section
|Usage={{TODO|The API name in the Syntax section should be ''data'', not ''data (TextNode)''.}}
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 1
|URL=http://www.w3.org/TR/REC-DOM-Level-1/
|Status=Recommendation
|Relevant_changes=Section 1.2
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/TextNode|TextNode]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}