{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The key value for the record currently displayed by the cursor.}}
{{API_Object_Property
|Property_applies_to=apis/indexeddb/IDBCursor
|Read_only=Yes
|Example_object_name=cursor
|Javascript_data_type=any
|Return_value_description=The value depends on the source of the value.  For more info, see the following Notes section.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The value of the '''key''' property depends on the [[apis/indexedDB/properties/source|'''source''']] of the [[apis/indexedDB/IDBCursor|'''cursor''']].

If the cursor is opened using an index, the return value represents the value of the attribute associated with the index.  If the cursor is opened using an obejct store, the return value represents the record's primary key.  If the cursor record is iterating to a new record or is outside the range of the cursor, the return value is "undefined".
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/indexedDB/IDBCursor|IDBCursor]]</code>
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}