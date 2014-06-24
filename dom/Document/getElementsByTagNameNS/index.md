{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs example and compat tables
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets a live HTMLCollection of the elements with the specified tag name and namespace.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=namespace
|Data type=String
|Description=The namespace URI that defines the desired elements or an asterisk (*) to match all namespaces with the document, or null.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=localName
|Data type=String
|Description=The name of the desired element or an asterisk (*) to match all elements with the specified namespace.
|Optional=No
}}
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=elements
|Javascript_data_type=Object
|Return_value_description=A live HTMLCollection of elements.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=This method should not be used. For a more performant alternative, see the notes.

Use this method to get a live list of elements with a specified name and namespace.
|Notes=*For performance reasons, [[css/selectors_api/querySelectorAll|'''querySelectorAll''']] is preferred, because it gets a static list.
*This method returns a live element list that gets updated whenever an element is added or removed from the document, this has performance implications and may result in unexpected errors (removing elements within a for loop while caching the length of the collection).
*If namespaces are irrelevant in the context, [[dom/HTMLElement/getElementsByTagName|getElementsByTagName]] can be used (but it is also not recommended; see the first two notes).
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/
|Status=Living Standard
|Relevant_changes=Section 6.5, 6.8
}}{{Related Specification
|Name=DOM Level 4
|URL=http://www.w3.org/TR/2014/CR-dom-20140508/#dom-document-getelementsbytagnamens
|Status=Candidate Recommendation
|Relevant_changes=No change
}}{{Related Specification
|Name=Document Object Model (DOM) Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.4
}}{{Related Specification
|Name=Document Object Model (DOM) Level 2 Core
|URL=http://www.w3.org/TR/DOM-Level-2-Core/
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}