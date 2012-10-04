{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=count|Data type=Integer|Description=A positive, non-zero  integer value indicating the number of records to advance.|Optional=}}
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
|name: TransactionInactiveError
|The transaction associated with the cursor  is not active.
|-
|name: InvalidStateError

code: DOMException.INVALID_STATE_ERR (11)
|The cursor is already advancing to a new position; that is, an advance request is already being processed.
|-
|name: TypeMismatchError

code: DOMException.TYPE_MISMATCH_ERROR  (17)
|The value of the count parameter is negative,  zero ("0"), or not a number.
|}
 


}}
{{Topics|DOM}}
{{Notes_Section
|Import_Notes=
===Syntax===
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