{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|This method creates and returns a new index with the given name and parameters in the connected database.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=Name of the index.
|Optional=No
}}{{Method Parameter
|Name=keyPath
|Data type=String
|Description=Name of the field to be indexed.
|Optional=No
}}{{Method Parameter
|Name=optionalParameters
|Data type=String
|Description=The options object whose attributes are optional parameters to this function. 'unique' specifies whether the index's unique flag is set. 'multiEntry' specifies whether the index's multiEntry flag is set.
|Optional=Yes
}}
|Method_applies_to=apis/indexeddb/IDBObjectStore
|Example_object_name=objectStore
|Return_value_name=index
|Javascript_data_type=DOM Node
|Return_value_description=[[apis/indexedDB/IDBIndex|'''IDBIndex''']]

An object representing the new index.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=// The transaction is already created

var objectStore = transaction.objectStore("ObjectStore_BookList");
var index = objectStore.createIndex("priceIndex", "price", {
    "unique": false,
    "multiEntry": true
});
|LiveURL=http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Create%20Index&
}}
}}
{{Notes_Section
|Notes=The method throws an exception if 

* This method was not called from a "versionchange" transaction callback. Also occurs if a request is made on a source object that has been deleted or removed.
* An index with the same name, compared in a case-sensitive manner, already exists in the connected database.
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