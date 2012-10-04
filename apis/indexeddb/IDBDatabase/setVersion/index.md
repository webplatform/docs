{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=version|Data type=DOMString|Description=The new version identifier.|Optional=}}
{{Method Parameter|Name=retVal|Data type=IDBVersionChangeRequest|Description=The transaction associated with the VERSION_CHANGE request.|Optional=}}
|Method_applies_to=apis/indexedDB/IDBDatabase
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code/value
!Description
|-
|S_OK
|
|-
|IDBDatabaseException.NOT_ALLOWED_ERR
6
|The data source has been deleted or is otherwise not available.
|}
 

IDBVersionChangeRequest

The transaction associated with the VERSION_CHANGE request.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The '''setVersion''' method was specified by an early draft of the [http://go.microsoft.com/fwlink/p/?LinkID{{=}}224519 Indexed Database specification].  The method was removed from later drafts of the specification and is no longer supported.
To create object stores, indexes, and other IndexedDB objects, use the '''version''' parameter of the [[apis/indexedDB/methods/open|'''open''']] method of the [[apis/indexedDB/properties/indexedDB|'''indexedDB''']] property to  generate an [[apis/indexedDB/events/onupgradeneeded|'''onupgradeneeded''']] event.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/indexedDB/IDBDatabase|IDBDatabase]]</code>
*<code>[[apis/indexedDB/events/onupgradeneeded|onupgradeneeded]]</code>
*<code>[[apis/indexedDB/methods/open|open]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}