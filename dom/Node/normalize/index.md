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
{{Summary_Section|Merges adjacent DOM objects to produce a normalized document object model.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Node
|Example_object_name=node
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=By calling ''object.'''''normalize''' before the subelements of an object are manipulated, you ensure that the document object model has a consistent structure.  The normal form is useful for operations that require a consistent document tree structure, and it ensures that the document object model view is identical when it is saved and reloaded.
|Notes=The '''normalize''' method does not merge adjacent '''CDATA''' sections, allowing for an inconsistent object model when '''CDATA''' sections are present.
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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=6
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.normalize Node.normalize]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536646(v=vs.85).aspx normalize Method]
|HTML5Rocks_link=
}}