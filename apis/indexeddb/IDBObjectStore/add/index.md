{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Adds a record to the specified object store.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=value
|Data type=String
|Description=The value must be valid for the Structured Cloning Algorithm.
|Optional=No
}}{{Method Parameter
|Name=key
|Data type=String
|Description=A key must be provided if the Object Store does not have a key path, or a key generator is not specified.
|Optional=Yes
}}
|Method_applies_to=apis/indexeddb/IDBObjectStore
|Example_object_name=objectStore
|Return_value_name=idbRequest
|Javascript_data_type=DOM Node
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var dbOpenRequest = window.indexedDB.open("BookShop1");
dbOpenRequest.onsuccess = function(event){
    var db = dbOpenRequest.result;
    var transaction = db.transaction(["ObjectStore_BookList"], IDBTransaction.READ_WRITE);	
	
	// The object store has a keyPath as "id". Hence no key is specified, but the value has id as a property
    var objectStore = transaction.objectStore("ObjectStore_BookList");
	
	// Sample data to add to the Object store
	var key = 10;
    var value = {
        "bookName": "Book-" + Math.random(),
        "author": "AuthorName",
        "id": key
    };
    
    var request = objectStore.add(value);
    request.onsuccess = function(event){
        console.log("Saved id ", request.result);
    };
    request.onerror = function(e){
		console.log("Error adding data")
    };
    
};
|LiveURL=http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#saveData&
}}
}}
{{Notes_Section
|Usage=An error is thrown if one of the following is true

*The object store uses in-line keys and the key parameter was provided.
*The object store uses out-of-line keys and has no key generator and the key parameter was not provided.
*The object store uses in-line keys and the result of evaluating the object store's key path yields a value and that value is not a valid key.
*The object store uses in-line keys but no key generator and the result of evaluating the object store's key path does not yield a value.
*The key parameter was provided but does not contain a valid key.
|Notes====Remarks===
This method can throw the following [[dom/DOMException|'''DOMException''']]
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Structured Cloning Algorithm
|URL=http://www.w3.org/TR/html5/common-dom-interfaces.html#safe-passing-of-structured-data
|Status=W3C Working Draft
}}
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