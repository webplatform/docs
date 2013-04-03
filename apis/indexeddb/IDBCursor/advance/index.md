{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Advances the cursor by the specified number.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=count
|Data type=Number
|Description=A positive, non-zero  integer value indicating the number of records to advance.
|Optional=No
}}
|Method_applies_to=apis/indexeddb/IDBCursor
|Example_object_name=cursor
|Javascript_data_type=void
|Return_value_description=Instead of creating a new IDBRequest object, this method reuses reuses the request originally created when this cursor was created.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var dbOpenRequest = window.indexedDB.open("BookShop1");
dbOpenRequest.onsuccess = function(event){
    var transaction = dbOpenRequest.result.transaction(["ObjectStore_BookList"], IDBTransaction.READ_WRITE);
    var objectStore = transaction.objectStore("ObjectStore_BookList");
    // Function to call when a new cursor is required
    var cursor = null;
    var request = objectStore.openCursor(IDBKeyRange.bound(0, new Date().getTime(), true, false), 1);
    request.onsuccess = function(event){
        cursor = request.result;
        write("Cursor opened", cursor);
        
        if (cursor) {
            write("Value in cursor now is ", cursor.key, cursor.value);
            cursor.advance(2); // jump 2 entries
        }
        
    };
};
|LiveURL=http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Advance%20cursor&
}}
}}
{{Notes_Section
|Usage=Throws an exception if 

* The value passed into the count parameter was zero or a negative number.
* The transaction this IDBCursor belongs to is not active.
* The cursor is currently being iterated, or has iterated past its end.
|Notes=Calling this method more than once before new cursor data has been loaded is not allowed and results in a DOMException of type InvalidStateError being thrown. For example, calling advance() twice from the same onsuccess handler results in a DOMException of type InvalidStateError being thrown on the second call.
|Import_Notes====Syntax===
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
*<code>[[apis/indexedDB/IDBCursor|IDBCursor]]</code>
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}