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
{{Summary_Section|Creates a structured clone of the value parameter.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=value
|Data type=Blob
|Description=An object literal containing the values to be stored in the object store.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=key
|Data type=Blob
|Description=The key value of the new record.
|Optional=No
}}
|Method_applies_to=apis/indexeddb/IDBObjectStore
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
'''name''': DataCloneError</dt>
<dt>
'''code''': DOMException.DATA_CLONE_ERR (25)</dt>
</dl>
{{!}}The data could not be saved to the object store.
{{!}}-
{{!}}<dl>
<dt>
'''name''': DataError</dt>
</dl>
{{!}}The specified '''key''' value is invalid or the value specified for an indexed attribute is invalid.
{{!}}-
{{!}}<dl>
<dt>
'''name''': InvalidStateError</dt>
<dt>
'''code''': DOMException.INVALID_STATE_ERR (11)</dt>
</dl>
{{!}}The object store has been deleted or is otherwise unavailable.
{{!}}-
{{!}}<dl>
<dt>
'''name''': ReadOnlyError</dt>
</dl>
{{!}}The associated transaction is read-only.
{{!}}-
{{!}}<dl>
<dt>
'''name''': TransactionInactiveError</dt>
</dl>
{{!}}The associated transaction is not active.
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