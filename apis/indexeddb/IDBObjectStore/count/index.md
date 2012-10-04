{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=key|Data type=any|Description=A key value or a reference to a [[apis/indexedDB/IDBKeyRange|'''IDBKeyRange''']] object.|Optional=}}
|Method_applies_to=apis/indexedDB/IDBObjectStore
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=[[apis/indexedDB/IDBRequest|'''IDBRequest''']]

The number of records matching the specified value or "0" if no matches are found.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
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
|The value specified for the '''key''' parameter is not a valid key value.
|-
|<dl>
<dt>
[[dom/properties/toString (DOMError)|'''name''']]: InvalidStateError</dt>
<dt>
[[dom/properties/code|'''code''']]: DOMException.INVALID_STATE_ERR (11)</dt>
</dl>
|The cursor underlying the request has been deleted or removed.
|}
 
'''Note'''  As of Internet Explorer 10, the [[dom/properties/code|'''code''']] property is deprecated in favor of the [[dom/properties/toString (DOMError)|'''name''']] property, which is preferred for standards compliance and future compatibility.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/indexedDB/IDBObjectStore|IDBObjectStore]]</code>
*<code>[[apis/indexedDB/IDBIndex|IDBIndex]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}