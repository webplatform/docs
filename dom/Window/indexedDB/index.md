{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/window
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
For security reasons, support for the [[apis/indexedDB/IDBFactory|'''indexedDB''']] property is limited to Metro style apps and to webpages loaded using the "http://" or "https://" protocols.
To troubleshoot webpages that incorporate IndexedDB features before uploading them to a public server, use a [ http://go.microsoft.com/fwlink/p/?LinkId{{=}}249011 local web server] to preview the pages using the loopback address (127.0.0.1).
'''Note'''  In pre-release versions of Internet Explorer 10, the [[apis/indexedDB/IDBFactory|'''indexedDB''']] was accessed using a vendor prefix ('''msIndexedDB''').  Such use is considered obsolete; applications using the vendor prefix should be updated to ensure standards-compliance and future compatibility.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Window</code>
*<code>[[apis/workers/objects/Worker|Worker]]</code>
*<code>[[apis/workers/objects/WorkerGlobalScope|WorkerGlobalScope]]</code>
*<code>[[apis/indexedDB/events/onsuccess|onsuccess]]</code>
*<code>[[apis/indexedDB/events/onerror|onerror]]</code>
*<code>onblocked</code>
*<code>[[apis/indexedDB/events/onupgradeneeded|onupgradeneeded]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}