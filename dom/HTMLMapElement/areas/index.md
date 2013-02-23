{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns an HTMLCollection of [[dom/HTMLAreaElement|area]] elements included within the element.}}
{{API_Object_Property
|Property_applies_to=dom/HTMLMapElement
|Read_only=Yes
|Example_object_name=mapElement
|Return_value_name=areaElements
|Javascript_data_type=Object
|Return_value_description=An HTMLCollection of [[dom/HTMLAreaElement|area]] elements.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Areas can be added to or removed from the collection. If duplicate identifiers are found, a collection of those items is returned. Collections of duplicates must be referenced subsequently by ordinal position.
To add elements to the collection, use the [[dom/methods/createElement|'''createElement''']] and [[dom/methods/add|'''add''']] methods.  Alternatively, use the [[dom/methods/insertAdjacentHTML|'''insertAdjacentHTML''']] method.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 HTML
|URL=http://www.w3.org/TR/DOM-Level-2-HTML/
|Status=Recommendation
|Relevant_changes=Section 1.6.5
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