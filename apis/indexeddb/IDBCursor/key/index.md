{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=apis/indexedDB/IDBCursor
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The value of the '''key''' property depends on the [[apis/indexedDB/properties/source|'''source''']] of the [[apis/indexedDB/IDBCursor|'''cursor''']].

{| class="wikitable"
|-
!Cursor Source
!Value
|-
|[[apis/indexedDB/IDBIndex|'''index''']]
|The attribute associated with the index.
|-
|[[apis/indexedDB/IDBObjectStore|'''object store''']]
|The value of the record's [[apis/indexedDB/properties/primaryKey|'''primary key''']].
|}
 
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/indexedDB/IDBCursor|IDBCursor]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}