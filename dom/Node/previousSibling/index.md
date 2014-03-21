{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Retrieves the previous child node of the parent of the node.}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=Yes
|Example_object_name=node
|Return_value_name=previousNode
|Javascript_data_type=DOM Node
|Return_value_description=The previous child node of the parent of the node, or null if the node is the first child.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''previousSibling''' property to obtain the previous sibling of a list item.
|Code=&lt;script&gt;
// returns the list item labeled 'List Item 1'
var oSibling {{=}} document.getElementById("oList").childNodes[1].previousSibling;
&lt;/script&gt;
&lt;body&gt;
 &lt;ul id{{=}}"oList"&gt;
  &lt;li&gt;List Item 1&lt;/li&gt;
  &lt;li&gt;List Item 2&lt;/li&gt;
  &lt;li&gt;List Item 3&lt;/li&gt;
 &lt;/ul&gt;
&lt;/body&gt;
}}
}}
{{Notes_Section}}
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