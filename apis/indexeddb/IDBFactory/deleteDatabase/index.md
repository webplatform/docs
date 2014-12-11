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
{{Summary_Section|Deletes a database with the specified name.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=name
|Data type=String
|Description=The name of the database to delete.
|Optional=No
}}
|Method_applies_to=apis/indexeddb/IDBFactory
|Example_object_name=window.indexeddb
|Return_value_name=dbOpenRequest
|Javascript_data_type=DOM Node
|Return_value_description=An '''IDBOpenRequest''' request object that fires events to indicate the result of the request.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Delete a database
|Code=var dbDeleteRequest = window.indexedDB.deleteDatabase("BookShop1");
  dbDeleteRequest.onsuccess = function(e){
    write("Database successfully deleted");
    
  };
  
  dbDeleteRequest.onerror = function(e){
    write("Error deleting DB");
  };
  dbDeleteRequest.onblocked = function(e){
    write("Deleting DB Blocked");
  };
|LiveURL=http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#deleteDB&
}}
}}
{{Notes_Section
|Usage=
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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=11
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
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