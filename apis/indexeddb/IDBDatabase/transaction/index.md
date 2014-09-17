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
{{Summary_Section|Execute the steps for creating a transaction in a sychronous fashion.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=storeNames
|Data type=Blob
|Description=If specified, defines the names of the object stores included in the transaction.  Use a '''DOMString''' to specify a single object store or an array of '''DOMString''' values to specify multiple object stores.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=mode
|Data type=Blob
|Description=Value
Meaning




readonly



Changes are not allowed in this transaction.






readwrite



Changes are allowed in this transaction.






versionchange



Objects in the database can be create
|Optional=No
}}
|Method_applies_to=apis/indexeddb/IDBDatabase
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
This method can throw the following [[dom/DOMException|'''DOMException''']] exceptions:
{{{!}} class="wikitable"
{{!}}-
{{!}}'''Exception properties'''
{{!}}'''Description'''
{{!}}-
{{!}}<dl>
<dt>
'''name''': InvalidAccessError</dt>
<dt>
'''code''': DOMException.INVALID_ACCESS_ERR (15)</dt>
</dl>
{{!}}The value of the '''storeNames''' parameter is blank or otherwise invalid.
{{!}}-
{{!}}<dl>
<dt>
'''name''': InvalidStateError</dt>
<dt>
'''code''': DOMException.INVALID_STATE_ERR (11)</dt>
</dl>
{{!}}The database has been closed or a transaction has been requested for an object that has been deleted or is otherwise unavailable.
{{!}}-
{{!}}<dl>
<dt>
'''name''': NotFoundError</dt>
<dt>
'''code''': DOMException.NOT_FOUND_ERR (8)</dt>
</dl>
{{!}}A specified object store could not be found in the current database  (case-sensitive).
{{!}}-
{{!}}<dl>
<dt>
'''name''': TypeError</dt>
</dl>
{{!}}The value of the '''mode''' parameter is not supported.
{{!}}}
 
'''Note'''  As of Internet Explorer 10, the '''code''' property is deprecated in favor of the '''name''' property, which is preferred for standards compliance and future compatibility.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]
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