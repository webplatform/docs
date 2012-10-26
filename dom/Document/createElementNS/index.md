{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Creates an element from the specified namespace.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=namespace
|Data type=String
|Description=The URI of the desired namespace.
|Optional=No
}}{{Method Parameter
|Name=tagName
|Data type=String
|Description=The name of the desired element.
|Optional=No
}}
|Method_applies_to=dom/document
|Example_object_name=document
|Return_value_name=element
|Javascript_data_type=DOM Node
|Return_value_description=The created element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following  code example creates a circle element from the SVG namespace.
|Code=var sNamespace {{=}} "http://www.w3.org/2000/svg";
var oCircle {{=}} document.createElementNS(sNamespace, "circle");
}}
}}
{{Notes_Section
|Notes=The '''createElementNS''' method is supported only for XML namespaces.
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}