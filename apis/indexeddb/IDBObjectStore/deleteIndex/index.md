{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|This method destroys the index with the given name in the connected database. Note that this method must only be called from a "versionchange" transaction callback.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=indexName
|Data type=String
|Description=Name of the index to be deleted.
|Optional=No
}}
|Method_applies_to=apis/indexeddb/IDBObjectStore
|Example_object_name=objectStore
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var objectStore = transaction.objectStore("ObjectStore_BookList");
objectStore.deleteIndex("priceIndex");
|LiveURL=http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Delete%20Index&
}}
}}
{{Notes_Section
|Notes=Throws an exception when 
* This method was not called from a "versionchange" transaction callback.
* There is no index with the given name, compared in a case-sensitive manner, in the connected database.
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