{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the value of a content attribute in a specified namespace.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=namespaceURI
|Data type=String
|Description=The namespace URI of the attribute, or null.
|Optional=No
}}{{Method Parameter
|Name=name
|Data type=String
|Description=The local name of the attribute within the specified namespace.
|Optional=No
}}{{Method Parameter
|Name=value
|Data type=String
|Description=The value of the attribute.
|Optional=No
}}
|Method_applies_to=dom/Element
|Example_object_name=element
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Use this method to set an attribute in a specified namespace.
|Notes=*Where namespaces are irrelevant, [[dom/methods/setAttribute|setAttribute]] can be used instead.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Document Object Model (DOM) Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.4
}}{{Related Specification
|Name=Document Object Model (DOM) Level 2 Core
|URL=http://www.w3.org/TR/DOM-Level-2-Core/
|Status=Recommendation
|Relevant_changes=Section 1.2
}}{{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/
|Status=Living Standard
|Relevant_changes=Section 6.8
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