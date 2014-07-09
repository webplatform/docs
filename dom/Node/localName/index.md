{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs example
Must be served with XML content type, such as text/xml or application/xhtml+xml
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Retrieves the local name of the fully qualified XML declaration for a node.}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=Yes
|Example_object_name=node
|Return_value_name=localName
|Javascript_data_type=String
|Return_value_description=The local name portion of the '''qualified name''' of the node.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=In XML documents, elements can be declared using ''qualified names'', which consist of a [[dom/Node/prefix|'''prefix''']] and a local name. This property returns the latter value.
For more information, see [http://go.microsoft.com/fwlink/p/?linkid{{=}}203781 W3C Namespaces in XML].
|Notes=Must be served with XML content type, such as text/xml or application/xhtml+xml
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.localName Node.localName]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974770(v=vs.85).aspx localName Property]
|HTML5Rocks_link=
}}