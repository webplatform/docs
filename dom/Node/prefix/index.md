{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
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
|Examples={{Single Example
|Language=HTML
|Description=This example will only work when a namespace-aware parser is used, i.e. when a document is served with an XML mime-type. This will not work for HTML documents.
|Code=&lt;x:div onclick="alert(this.prefix)"/&gt;
}}
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.prefix Node.prefix]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974772(v=vs.85).aspx prefix Property]
|HTML5Rocks_link=
}}