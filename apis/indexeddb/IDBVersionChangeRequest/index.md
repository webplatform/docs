{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Deprecated. Previously used to change the version of the database.}}
{{API_Object
|Subclass_of=
|Overview=
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Usage=
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
{{See_Also_Section
|Manual_links=
|External_links=
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
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}