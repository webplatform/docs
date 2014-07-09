{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=needs example
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets the URI of the namespace associated with a namespace prefix, if any.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=prefix
|Data type=String
|Description=The prefix, or null.
|Optional=No
}}
|Method_applies_to=dom/Node
|Example_object_name=node
|Return_value_name=namespaceURI
|Javascript_data_type=String
|Return_value_description=The URI of the namespace for '''prefix'''.
null if no namespace is found for '''prefix'''.
The default namespace if '''prefix''' is null.
}}
{{Examples_Section
|Not_required=No
|Examples=
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.namespaceURI Node.namespaceURI]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974771(v=vs.85).aspx namespaceURI Property]
|HTML5Rocks_link=
}}