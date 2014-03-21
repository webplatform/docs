{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Retrieves the type of the requested node.}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=Yes
|Example_object_name=node
|Return_value_name=nodeType
|Javascript_data_type=Number
|Return_value_description=One of the node type constants defined on [[dom/Node|Node]], or null.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example assigns the '''nodeType''' property of the '''body''' object to a variable.
|Code=var iType {{=}} document.body.nodeType;
}}{{Single Example
|Language=JavaScript
|Description=This example assigns the '''nodeType''' property of a node created with the [[dom/Document/createElement|'''createElement''']] method to a variable.
|Code=var oNode {{=}} document.createElement("B");
document.body.insertBefore(oNode);
var iType {{=}} oNode.nodeType;
}}
}}
{{Notes_Section
|Notes=If the node represents an attribute retrieved from the [[dom/Node/attributes|'''attributes''']] collection, the '''nodeType''' returns <code>null</code>.
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
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=6 and later
|Note=This property applies to the [[dom/attributes|'''attribute''']] object.
}}
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