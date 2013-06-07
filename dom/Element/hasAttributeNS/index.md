{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Determines whether a content attribute in a specified namespace exists on an element.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=namespaceURI
|Data type=String
|Description=The namespace URI that defines the attribute name, or null.
|Optional=No
}}{{Method Parameter
|Name=name
|Data type=String
|Description=The name of the attribute.
|Optional=No
}}
|Method_applies_to=dom/Element
|Example_object_name=element
|Return_value_name=attributeExists
|Javascript_data_type=Boolean
|Return_value_description=Whether the specified attribute exists.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Use this method to determine whether a content attribute in a specified namespace exists on an element.
|Notes=*This method does not get the value of the attribute, see [[dom/methods/getAttributeNS|getAttributeNS]] for this purpose.
*Where namespaces are irrelevant, [[dom/methods/hasAttribute|hasAttribute]] can be used instead.
*See [[dom/methods/hasAttributes|hasAttributes]], which determines whether the element has any attributes at all.
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