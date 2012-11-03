{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/indexedDB/IDBTransaction
|Example_object_name=transaction
|Javascript_data_type=void
|Return_value_description=No return value
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=/*Open Database*/
var dbOpenRequest = window.indexedDB.open("BookShop1");
dbOpenRequest.onsuccess = function (event) {
    var db = dbOpenRequest.result;
    try {
        var transaction = db.transaction(["ObjectStore_BookList"], IDBTransaction.READ_WRITE);

        // Now that the transaction is created, lets abort it !! 
        transaction.abort();
    } catch (e) {
        write("Could not open transaction");
    }
};
|LiveURL=http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Abort Transaction&
}}
}}
{{Notes_Section
|Usage=If the transaction is finished, a DOMException of type InvalidStateError is thrown. Otherwise, the steps to abort a transactions are run.
|Import_Notes====Standards information===
*[http://www.w3.org/TR/IndexedDB/#widl-IDBTransaction-abort-void Indexed Database API]
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=24
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=11
|Firefox_supported=Yes
|Firefox_version=16
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=4
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages===
*<code>[[apis/indexedDB/IDBTransaction|IDBTransaction]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
}






}





}}