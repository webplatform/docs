{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The open method is used to open an IndexedDB database.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=The name of the database to be opened.
|Optional=No
}}{{Method Parameter
|Name=version
|Data type=Number
|Description=The version (unsigned long long) for the database
|Optional=Yes
}}
|Method_applies_to=apis/indexeddb/IDBFactory
|Example_object_name=indexeddb
|Return_value_name=dbOpenRequest
|Javascript_data_type=DOM Node
|Return_value_description=[[apis/indexedDB/IDBOpenRequest|'''IDBOpenRequest''']]

A [[apis/indexedDB/IDBOpenRequest|'''IDBOpenRequest''']] request object that fires events to indicate the result of the request.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Open a database without a version number
|Code=var dbOpenRequest = window.indexedDB.open("DatabaseName");
  dbOpenRequest.onsuccess = function(event){
var db = dbOpenRequest.result; // This is the database object
};


dbOpenRequest.onerror = function(e){
   // Called when an error occurs
  };
  dbOpenRequest.onblocked = function(e){
    // Called if another transaction is open on the database
  };
|LiveURL=http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#db
}}{{Single Example
|Language=JavaScript
|Description=Open a database with a version number that is higher than the existing version number
|Code=// The database is already opened with version 1. 
var dbOpenRequest = window.indexedDB.open("DatabaseName", 2);
  dbOpenRequest.onsuccess = function(event){
var db = dbOpenRequest.result; // This is the database object on which various operations can be performed
};

dbOpenRequest.onupgradeneeded = function(e){
   //This occurs when the version specified in the open call is higher that the version of the database. This is the version change transaction. 
  };
dbOpenRequest.onerror = function(e){
   // Called when an error occurs
  };
  dbOpenRequest.onblocked = function(e){
    // Called if another transaction is open on the database
  };
|LiveURL=http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#dbVersion&
}}
}}
{{Notes_Section
|Usage=var openRequest = window.indexedDB.open("databaseName", 1);
|Notes=The open method either creates a database if it does not exist, or opens one, with the specified version number. If no version number is specified, the database is opened with the current version number. If a database is to be created and a version number is not specified, the database is opened with a version 1.
|Import_Notes====Standards information===
*[http://www.w3.org/TR/IndexedDB/#widl-IDBFactory-open-IDBOpenDBRequest-DOMString-name-unsigned-long-long-version Indexed Database API - open Method]
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=open method
|Chrome_supported=Yes
|Chrome_version=11
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4
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
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=10
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Yes
|Chrome_mobile_prefixed_version=18
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Yes
|Firefox_mobile_prefixed_version=15
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/indexedDB/properties/indexedDB|indexedDB]]</code>
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}