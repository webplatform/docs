{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=key|Data type=any|Description=If specified, the cursor skips the number of objects specified by the value of this parameter.  If blank or not specified, the next object is selected.|Optional=}}
|Method_applies_to=apis/indexedDB/IDBCursor
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=

This method can throw the following [[dom/DOMException|'''DOMException''']] exceptions:

'''Note'''  As of Internet Explorer 10, the [[dom/properties/code|'''code''']] property is deprecated in lieu of the [[dom/properties/toString (DOMError)|'''name''']] property, which is preferred for standards compliance and future compatibility.

{| class="wikitable"
|-
!Exception properties
!Description
|-
|name: DataError
|The value specified for the key parameter is not valid.
|-
|name: TransactionInactiveError
|The transaction associated with the cursor  is not active.
|-
|name: InvalidStateError

code: DOMException.INVALID_STATE_ERR (11)
|The cursor is already iterating or has reached the last object.
|}
 


}}
{{Topics|DOM}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/indexedDB/IDBCursor|IDBCursor]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}