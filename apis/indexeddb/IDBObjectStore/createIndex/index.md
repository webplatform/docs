{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Proposed Recommendation}}
{{API_Name}}
{{Summary_Section|This method creates and returns a new index with the given name and parameters in the connected database.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=name
|Data type=String
|Description=Name of the index.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=keyPath
|Data type=String
|Description=Name of the field to be indexed.
|Optional=No
}}{{Method Parameter
|Index=2
|Name=optionalParameters
|Data type=String
|Description=The options object whose attributes are optional parameters to this function. 'unique' specifies whether the index's unique flag is set. 'multiEntry' specifies whether the index's multiEntry flag is set.
|Optional=Yes
}}
|Method_applies_to=apis/indexeddb/IDBObjectStore
|Example_object_name=objectStore
|Return_value_name=index
|Javascript_data_type=DOM Node
|Return_value_description='''IDBIndex'''

An object representing the new index.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
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
|Usage=
|Notes=The method throws an exception if 

* This method was not called from a "versionchange" transaction callback. Also occurs if a request is made on a source object that has been deleted or removed.
* An index with the same name, compared in a case-sensitive manner, already exists in the connected database.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C IndexedDB Specification
|URL=http://www.w3.org/TR/IndexedDB/
|Status=W3C Proposed Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}