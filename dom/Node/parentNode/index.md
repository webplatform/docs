{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Retrieves the parent node in the document hierarchy.}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=Yes
|Example_object_name=node
|Return_value_name=parentNode
|Javascript_data_type=DOM Node
|Return_value_description=The parent node of the node.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example assigns the '''parentNode''' of a '''span''' object to a variable.
|Code=&lt;script&gt;
var oParent {{=}} document.getElementById("oSpan").parentNode;
&lt;/script&gt;
:
&lt;body&gt;
&lt;span ID{{=}}"oSpan"&gt;A Span&lt;/span&gt;
&lt;/body&gt;
}}{{Single Example
|Language=JavaScript
|Description=This example assigns the '''parentNode''' of a node, created with the [[dom/methods/createElement|'''createElement''']] method, to a variable.
|Code=var oNode {{=}} document.createElement("B");
document.body.insertBefore(oNode);
// This returns document.body.
var oParent {{=}} oNode.parentNode;
}}
}}
{{Notes_Section
|Notes=The topmost object returns null as its parent.
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}