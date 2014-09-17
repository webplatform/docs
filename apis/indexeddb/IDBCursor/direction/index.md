{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs example, spec reference
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Indicates the direction of travel within a cursor.}}
{{API_Object_Property
|Property_applies_to=apis/indexeddb/IDBCursor
|Read_only=Yes
|Example_object_name=cursor
|Return_value_name=
|Javascript_data_type=String
|Return_value_description=The return value describes the direction of travel and the uniqueness of data within the cursor.  It corresponds to one of the following:

; next
: The cursor is travelling in ascending order and contains all matching records, including duplicate values.
;nextunique
:The cursor is travelling in ascending order and contains just one instance of matching key values.
;prev
:The cursor is travelling in descending order and all matching records, including duplicate values.
;prevunique
:The cursor is travelling in descending order and contains just one instance of matching key values.
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Indexed Database API
|URL=http://www.w3.org/TR/IndexedDB/
|Status=Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
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
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
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