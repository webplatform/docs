{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs example, spec reference, standardization status
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The key value for the record currently displayed by the cursor.}}
{{API_Object_Property
|Property_applies_to=apis/indexeddb/IDBCursor
|Read_only=Yes
|Example_object_name=cursor
|Return_value_name=
|Javascript_data_type=any
|Return_value_description=The value depends on the source of the value.  For more info, see the following Notes section.
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The value of the '''key''' property depends on the '''source''' of the '''cursor'''.

If the cursor is opened using an index, the return value represents the value of the attribute associated with the index.  If the cursor is opened using an obejct store, the return value represents the record's primary key.  If the cursor record is iterating to a new record or is outside the range of the cursor, the return value is "undefined".
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]
}}
{{Related_Specifications_Section
|Specifications=
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}