{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets the name of a particular type of node.}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=Yes
|Example_object_name=node
|Return_value_name=nodeName
|Javascript_data_type=String
|Return_value_description=The name of the node.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following code example uses the '''nodeName''' property to obtain the name of an element.
|Code=&lt;script&gt;
// returns the element name 'LI' of the list item labeled 'List Item 2'
var sName {{=}} document.getElementById("oList").childNodes(1).nodeName;
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
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
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