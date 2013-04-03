{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The mode for isolating access to data in the object stores that are in the scope of the transaction. For possible values, see Return Value, below. The default value is readonly.}}
{{API_Object_Property
|Property_applies_to=apis/indexeddb/IDBTransaction
|Read_only=Yes
|Javascript_data_type=String
|Return_value_description=* readonly (0) - Allows data to be read but not changed.
* readwrite (1) - Allows reading and writing of data in existing data stores to be changed.
* versionchange (2) - Allows any operation to be performed, including ones that delete and create object stores and indexes. This mode is for updating the version number of transactions that were started using the setVersion() method of IDBDatabase objects. Transactions of this mode cannot run concurrently with other transactions.
}}
{{Examples_Section
|Not_required=No
|Examples=
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
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/indexedDB/IDBTransaction|IDBTransaction]]</code>
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/IndexedDB/IDBTransaction
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}