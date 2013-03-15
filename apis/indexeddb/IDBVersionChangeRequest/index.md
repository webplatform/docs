{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Deprecated. Previously used to change the version of the database.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The '''IDBVersionChangeRequest''' object was returned by the [[apis/indexedDB/methods/setVersion|'''setVersion''']] method, as specified by an early draft of the [http://go.microsoft.com/fwlink/p/?LinkID{{=}}224519 Indexed Database specification].  The object and method were removed from later drafts of the specification and are no longer supported.
To create object stores, indexes, and other IndexedDB objects, use the '''version''' parameter of the [[apis/indexedDB/methods/open|'''open''']] method of the [[apis/indexedDB/properties/indexedDB|'''indexedDB''']] property to  generate an [[apis/indexedDB/events/onupgradeneeded|'''onupgradeneeded''']] event.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]


===Members===
The '''IDBVersionChangeRequest''' object does not define any members.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/indexedDB/events/onupgradeneeded|onupgradeneeded]]</code>
*<code>[[apis/indexedDB/methods/open|open]]</code>
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}