{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/window
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
For security reasons, support for the [[apis/indexedDB/IDBFactory|'''indexedDB''']] property is limited to Metro style apps and to webpages loaded using the "http://" or "https://" protocols.
To troubleshoot webpages that incorporate IndexedDB features before uploading them to a public server, use a [ http://go.microsoft.com/fwlink/p/?LinkId{{=}}249011 local web server] to preview the pages using the loopback address (127.0.0.1).
'''Note'''  In pre-release versions of Internet Explorer 10, the [[apis/indexedDB/IDBFactory|'''indexedDB''']] was accessed using a vendor prefix ('''msIndexedDB''').  Such use is considered obsolete; applications using the vendor prefix should be updated to ensure standards-compliance and future compatibility.
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
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=10
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>Window</code>
*<code>[[apis/workers/objects/Worker|Worker]]</code>
*<code>[[apis/workers/objects/WorkerGlobalScope|WorkerGlobalScope]]</code>
*<code>[[apis/indexedDB/events/onsuccess|onsuccess]]</code>
*<code>[[apis/indexedDB/events/onerror|onerror]]</code>
*<code>onblocked</code>
*<code>[[apis/indexedDB/events/onupgradeneeded|onupgradeneeded]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}