{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The createObjectStore method enables you to create object stores inside an indexedDB database. The creation of an object store is only possible inside an "versionchange" transaction.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=The name of the object store to be created.
|Optional=No
}}{{Method Parameter
|Name=optionalParameters
|Data type=DOM Node
|Description=An object literal containing one or more of the following attributes:
* '''keyPath''': specifies the key path of the new object store. If the attribute is null, no key path is specified. In this case the key isn't an attribute of the object stored in the value
* '''autoIncrement''': specifies whether the object store should have a key generator. If a key generator is present, the key will be automatically incremented when objects get inserted.
|Optional=Yes
}}
|Method_applies_to=apis/indexeddb/IDBDatabase
|Example_object_name=IDBDatabase
|Return_value_name=IDBObjectStore
|Javascript_data_type=DOM Node
|Return_value_description=[[apis/indexedDB/IDBObjectStore|'''IDBObjectStore''']]

An object representing the new object store.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=// the db object was opened in the upgradeNeeded method
try {
  var objectStore = db.createObjectStore("ObjectStore_BookList", {
    "keyPath": "id",
    "autoIncrement": true
  });
  write("Object Store created", objectStore);
} catch (e) {
  write("Error occured", e);
}​
|LiveURL=http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#createObjectStore&
}}
}}
{{Notes_Section
|Notes=The method throws an exception if 

* This method was not called from a "versionchange" transaction. Also occurs if a request is made on a source object that has been deleted or removed.
* If an object store with the same name, compared in a case-sensitive manner, already exists in the connected database.
* If autoIncrement is set to true, and keyPath either is the empty string, or an Array containing the empty string.
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
*<code>[[apis/indexedDB/IDBDatabase|IDBDatabase]]</code>
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}