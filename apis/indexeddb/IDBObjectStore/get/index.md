{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Runs the steps for asynchronously executing a request and returns the IDBRequest created by these steps.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=key
|Data type=Blob
|Description=The key value of the record to be retrieved.
|Optional=No
}}
|Method_applies_to=apis/indexeddb/IDBObjectStore
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
This method can throw the following [[dom/DOMException|'''DOMException''']] exceptions:
{| class="wikitable"
|-
|'''Exception properties'''
|'''Description'''
|-
|<dl>
<dt>
[[dom/properties/toString (DOMError)|'''name''']]: DataError</dt>
</dl>
|The '''key''' parameter value is not valid.
|-
|<dl>
<dt>
[[dom/properties/toString (DOMError)|'''name''']]: InvalidStateError</dt>
<dt>
[[dom/properties/code|'''code''']]: DOMException.INVALID_STATE_ERR (11)</dt>
</dl>
|The object store has been deleted or is otherwise unavailable.
|-
|<dl>
<dt>
[[dom/properties/toString (DOMError)|'''name''']]: TransactionInactiveError</dt>
</dl>
|The associated transaction is not active.
|}
 
'''Note'''  As of Internet Explorer 10, the [[dom/properties/code|'''code''']] property is deprecated in favor of the [[dom/properties/toString (DOMError)|'''name''']] property, which is preferred for standards compliance and future compatibility.
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
*<code>[[apis/indexedDB/IDBObjectStore|IDBObjectStore]]</code>
*<code>[[apis/indexedDB/IDBIndex|IDBIndex]]</code>
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}