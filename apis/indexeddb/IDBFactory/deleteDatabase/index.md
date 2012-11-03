{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=The name of the database to delete.
|Optional=No
}}
|Method_applies_to=apis/indexedDB/IDBFactory
|Example_object_name=window.indexeddb
|Return_value_name=dbOpenRequest
|Javascript_data_type=DOM Node
|Return_value_description=[[apis/indexedDB/IDBOpenRequest|'''IDBOpenRequest''']]

A [[apis/indexedDB/IDBOpenRequest|'''IDBOpenRequest''']] request object that fires events to indicate the result of the request.
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
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]
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
|Chrome_prefixed_version=23
|Firefox_supported=Yes
|Firefox_version=16
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=15
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=Unknown
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
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/indexedDB/properties/indexedDB|indexedDB]]</code>
*<code>[[apis/indexedDB/IDBFactory|IDBFactory]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}