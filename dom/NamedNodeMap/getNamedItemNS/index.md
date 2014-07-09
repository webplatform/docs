{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Gets an attribute with a given name and a given namespace.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=namespace
|Data type=String
|Description=The namespace name of the attribute to get.
|Optional=No
}}{{Method Parameter
|Name=name
|Data type=String
|Description=The local name of the desired attribute within the specified namespace.
|Optional=No
}}
|Method_applies_to=dom/NamedNodeMap
|Example_object_name=attributes
|Return_value_name=attribute
|Javascript_data_type=DOM Node
|Return_value_description=The attribute with the name and namespace.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Create a SVG circle element.
|Code=var nsSVG='http://www.w3.org/2000/svg';
var osvgCircleTag=document.createElementNS(nsSVG,'circle');
alert(osvgCircleTag.getNamedItemNS(nsSVG,'r');
}}
}}
{{Notes_Section
|Usage=Used to create and manipulate XML and SVG documents.
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap NamedNodeMap]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975126(v=vs.85).aspx getNamedItemNS Method]
|HTML5Rocks_link=
}}