{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The error codes returned under certain conditions.}}
{{API_Object_Property
|Property_applies_to=apis/indexeddb/IDBRequest
|Read_only=Yes
|Javascript_data_type=DOMError
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=The following error codes are returned under certain conditions:

*AbortError — If you abort the transaction, then all requests still in progress receive this error.
*ConstraintError — If you insert data that doesn't conform to a constraint. It's an exception type for creating stores and indexes. You get this error, for example, if you try to add a new key that already exists in the record.
*QuotaExceededError — If you run out of disk quota and the user declined to grant you more space.
*UnknownError — If the operation failed for reasons unrelated to the database itself. A failure due to disk IO errors is such an example.
*NoError — If the request succeeds.
*VersionError — If you try to open a database with a version lower than the one it already has.

In addition to the error codes sent to the IDBRequest object, asynchronous operations can also raise exceptions. The list describes problems that could occur when the request is being executed, but you might also encounter other problems when the request is being made. For example, if the the request failed and the result is not available, the InvalidStateError exception is thrown.
|Notes====Remarks===
The cause of the error depends on the operation that triggered the error; use the [[dom/properties/toString (DOMError)|'''name''']] to determine the underlying problem.
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
*<code>[[apis/indexedDB/IDBRequest|IDBRequest]]</code>
*<code>[[apis/indexedDB/IDBTransaction|IDBTransaction]]</code>
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/IndexedDB/IDBRequest
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}