{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=name|Data type=DOMString|Description=Name of the object store to be removed.|Optional=}}
|Method_applies_to=apis/indexedDB/IDBDatabase
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
|name: InvalidStateError

code: DOMException.INVALID_STATE_ERR (11)
|The method was not called within the context of a VERSION_CHANGE transaction or the request was made for an object that has been moved or deleted.
|-
|name: NotFoundError

code: DOMException.NOT_FOUND_ERR (8)
|An object store could not be found with the specified name (case-sensitive).
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
*<code>[[apis/indexedDB/IDBDatabase|IDBDatabase]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}