{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Removes a record from the specified Object Store}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=key
|Data type=String
|Description=Key identifying the record to be deleted
|Optional=No
}}
|Method_applies_to=apis/indexeddb/IDBObjectStore
|Example_object_name=objectStore
|Return_value_name=idbRequest
|Javascript_data_type=DOM Node
|Return_value_description=Returns an IDBRequest Object
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=store = db.createObjectStore("store1", { autoIncrement: true });
store.put("a"); // Will get key 1
store.delete(1);
store.put("b"); // Will get key 2
store.clear();
store.put("c"); // Will get key 3
store.delete(IDBKeyRange.lowerBound(0));
|LiveURL=http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Delete%20Data&
}}
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
[[dom/properties/toString (DOMError)|'''name''']]: ReadOnlyError</dt>
</dl>
|The associated transaction is read-only.
|-
|<dl>
<dt>
[[dom/properties/toString (DOMError)|'''name''']]: TransactionInactiveError</dt>
</dl>
|The associated transaction is not active.
|}
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
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}