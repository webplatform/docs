{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs example, spec reference, standardization status
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The count method returns the number of records in an object store.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=key
|Data type=DOM Node
|Description=A key value or a reference to a [[apis/indexeddb/IDBKeyRange|'''IDBKeyRange''']] object.
|Optional=Yes
}}
|Method_applies_to=apis/indexeddb/IDBObjectStore
|Example_object_name=objectStore
|Return_value_name=recordCount
|Javascript_data_type=Number
|Return_value_description=[[apis/indexeddb/IDBRequest|'''IDBRequest''']]

The number of records matching the specified value or "0" if no matches are found.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=The method throws and exception is 

* The transaction this IDBObjectStoreSync belongs to is not active.
* The key parameter is not a valid key or a key range.
* Occurs if a request is made on a source object that has been deleted or removed.
|Import_Notes====Syntax===
}}
{{Related_Specifications_Section
|Specifications=
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