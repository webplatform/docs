{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the prefix of the fully qualified XML declaration for a node.}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=No
|Example_object_name=node
|Return_value_name=prefix
|Javascript_data_type=String
|Return_value_description=The prefix portion of the '''qualified name''' of the node.
|Example_value_name=newPrefix
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=In XML documents, elements can be declared using ''qualified names'', which consist of a prefix and a [[dom/Node/localName|'''localName''']]. This property returns the former value.
For more information, see [http://go.microsoft.com/fwlink/p/?linkid{{=}}203781 W3C Namespaces in XML].
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