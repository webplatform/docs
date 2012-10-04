{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=name|Data type=DOMString|Description=Name of the index.|Optional=}}
{{Method Parameter|Name=keyPath|Data type=any|Description=Name of the field to be indexed.|Optional=}}
{{Method Parameter|Name=optionalParameters|Data type=object|Description=An object literal containing one or more of the following attributes:|Optional=}}
|Method_applies_to=apis/indexedDB/IDBObjectStore
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=[[apis/indexedDB/IDBIndex|'''IDBIndex''']]

An object representing the new index.


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
[[dom/properties/toString (DOMError)|'''name''']]: ConstraintError</dt>
</dl>
|An index with the same name (case-sensitive) already exists in the database.
|-
|<dl>
<dt>
[[dom/properties/toString (DOMError)|'''name''']]: InvalidStateError</dt>
<dt>
[[dom/properties/code|'''code''']]: DOMException.INVALID_STATE_ERR (11)</dt>
</dl>
|Either the associated transaction is not a VERSION_CHANGE transaction or the object store has been deleted from the database.
|}
 
'''Note'''  As of Internet Explorer 10, the [[dom/properties/code|'''code''']] property is deprecated in favor of the [[dom/properties/toString (DOMError)|'''name''']] property, which is preferred for standards compliance and future compatibility.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/indexedDB/IDBObjectStore|IDBObjectStore]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}