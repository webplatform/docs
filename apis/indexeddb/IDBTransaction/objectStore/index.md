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
{{Summary_Section|Returns an object store that has already been added to the scope of this transaction.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=name
|Data type=any
|Description=Name of the object store to return.
|Optional=No
}}
|Method_applies_to=apis/indexeddb/IDBTransaction
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
{| class="wikitable"
|-
|'''Exception properties'''
|'''Description'''
|-
|<dl>
<dt>
[[dom/properties/toString (DOMError)|'''name''']]: NotFoundError</dt>
<dt>
[[dom/properties/code|'''code''']]: DOMException.NOT_FOUND_ERR (8)</dt>
</dl>
|An object store could not be found with the specified name (case-sensitive).
|-
|<dl>
<dt>
[[dom/properties/toString (DOMError)|'''name''']]: InvalidStateError</dt>
<dt>
[[dom/properties/code|'''code''']]: DOMException.INVALID_STATE_ERR (11)</dt>
</dl>
|The object store has been deleted or is otherwise unavailable.
|}
 
'''Note'''  As of Internet Explorer 10, the [[dom/properties/code|'''code''']] property is deprecated in favor of the [[dom/properties/toString (DOMError)|'''name''']] property, which is preferred for standards compliance and future compatibility.
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
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/indexedDB/IDBTransaction|IDBTransaction]]</code>
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