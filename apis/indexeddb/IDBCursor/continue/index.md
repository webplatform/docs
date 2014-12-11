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
{{Summary_Section|Moves to the next record, or to the record specified by a key.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=key
|Data type=String
|Description=The next key to position this cursor at.

If the key parameter is specified and fulfills any of these conditions this method must throw a DOMException of type DataError:

* The parameter is not a valid key.
* The parameter is less than or equal to this cursor's position and this cursor's direction is "next" or "nextunique".
* The parameter is greater than or equal to this cursor's position and this cursor's direction is "prev" or "prevunique".
|Optional=Yes
}}
|Method_applies_to=apis/indexeddb/IDBCursor
|Example_object_name=cursor
|Return_value_name=hasMoved
|Javascript_data_type=Boolean
|Return_value_description=If the steps for synchronously executing a request returns a cursor, then this function returns true. Otherwise this function returns false.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var tx = db.transaction('Contact');
var store = tx.objectStore('Contact');
var cursor = store.openCursor();
while(cursor.continue()) {
    var value = cursor.value;
    // act on each object or key
}
|LiveURL=http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Continue%20with%20cursor&
}}
}}
{{Notes_Section
|Usage=The continue method throws an exception if 

* The transaction this IDBCursor belongs to is not active.
* The cursor is currently being iterated, or has iterated past its end.
* The key parameter was specified but did not contain a valid key.
|Notes=
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