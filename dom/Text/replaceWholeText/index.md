{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example....
leave for me...
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section|Replaces the text of the current object.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=text
|Data type=String
|Description=The text that replaces the existing text.
|Optional=No
}}
|Method_applies_to=dom/Text
|Example_object_name=textNode
|Return_value_name=textNode
|Javascript_data_type=DOM Node
|Return_value_description=A [[dom/Text|'''Text''']] node that received the replacement text.  If the replaced text was empty, this value will be null. If the current node is read-only, a new '''Text''' node is returned. If the current node is not read-only, the same object is returned.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Obsolete

This feature is obsolete. Although it may still work in some browsers, its use is discouraged since it could be removed at any time. Try to avoid using it.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.2
}}{{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#text
|Status=Living Standard
|Relevant_changes=Removed from the spec
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
|Internet_explorer_version=9
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Text.replaceWholeText Text.replaceWholeText]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975208(v=vs.85).aspx replaceWholeText Method]
|HTML5Rocks_link=
}}