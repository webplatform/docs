{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Interface implemented by the [[apis/indexeddb/indexedDB|indexedDB]] object; provides for the creation and access of a database.}}
{{API_Object}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Use the [[apis/indexedDB/properties/indexedDB|'''indexedDB''']] property to access IndexedDB features supported by Internet Explorer 10 and Metro style apps
'''Important'''  For security reasons, support for the '''indexedDB''' property is limited to Metro style apps and to webpages loaded using the "http://" or "https://" protocols.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]


===Members===
The '''IDBFactory''' object has these types of members:
*[#methods Methods]


====Methods====
The '''IDBFactory''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|'''cmp'''
|Compares two values and indicates whether one is greater than the other.
|-
|[[apis/indexedDB/methods/deleteDatabase|'''deleteDatabase''']]
|Deletes a database.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=IDBFactory
|Chrome_supported=Yes
|Chrome_version=24
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=22
|Firefox_supported=Yes
|Firefox_version=16
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=15
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/window|window]]</code>
*<code>[[apis/indexedDB/events/onsuccess|onsuccess]]</code>
*<code>[[apis/indexedDB/events/onerror|onerror]]</code>
*<code>onblocked</code>
}}
{{Topics|IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}