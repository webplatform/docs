{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Creates a Document Type node.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=qualifiedName
|Data type=String
|Description=The name of the [[html/elements/!DOCTYPE|document type]].  When you use XML namespaces, this name can be a qualified name (for example, namespace:localname).
|Optional=No
}}{{Method Parameter
|Name=publicID
|Data type=String
|Description=The public identifier of the [[html/elements/!DOCTYPE|document type]] or null.
|Optional=No
}}{{Method Parameter
|Name=systemId
|Data type=String
|Description=The system identifier of the [[html/elements/!DOCTYPE|document type]] or null.
|Optional=No
}}
|Method_applies_to=dom/implementation
|Example_object_name=implementation
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=The created [[html/elements/!DOCTYPE|document type]] object.
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
*<code>[[dom/implementation|implementation]]</code>
*<code>Reference</code>
*<code>[[dom/methods/createDocument|createDocument]]</code>
*<code>[[dom/methods/createHTMLDocument|createHTMLDocument]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}