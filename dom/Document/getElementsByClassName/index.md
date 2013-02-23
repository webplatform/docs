{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Use [[css/selectors_api/querySelectorAll|<code>elementOrDocument.querySelectorAll(".class-name.other-class-name")</code>]] instead. Gets a collection of all descendant elements with given classes.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=classNames
|Data type=String
|Description=A space separated list of classes.
|Optional=No
}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=element
|Return_value_name=elements
|Javascript_data_type=Object
|Return_value_description=A live [[dom/HTMLCollection|HTMLCollection] of elements with the given class names.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=The use of this property is discouraged. See the [[#Notes|Notes]] section for details.
|Notes=The use of this property is discouraged, due to the performance implications (due to the live DOMCollection where any changes to the document must be reflected on the returned object immediately) and complexity (the removal of an element from the document will result in immediate changes to the collection).

A close alternative -
*[[css/selectors_api/querySelectorAll|<code>elementOrDocument.querySelectorAll(".class-name.other-class-name")</code>]]
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Candidate Recommendation
|Relevant_changes=Section 3.1.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
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