{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The createObjectStore method enables you to create object stores inside an indexedDB database. The creation of an object store is only possible inside an "versionchange" transaction.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=The name of the object store to be created.
|Optional=No
}}{{Method Parameter
|Name=optionalParameters
|Data type=DOM Node
|Description=An object literal containing one or more of the following attributes:
* '''keyPath''': specifies the key path of the new object store. If the attribute is null, no key path is specified. In this case the key isn't an attribute of the object stored in the value
* '''autoIncrement''': specifies whether the object store should have a key generator. If a key generator is present, the key will be automatically incremented when objects get inserted.
|Optional=Yes
}}
|Method_applies_to=apis/indexedDB/IDBDatabase
|Example_object_name=IDBDatabase
|Return_value_name=IDBObjectStore
|Javascript_data_type=DOM Node
|Return_value_description=[[apis/indexedDB/IDBObjectStore|'''IDBObjectStore''']]

An object representing the new object store.

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
|name: ConstraintError
|An object store in the database already uses the name (case-sensitive).
|-
|name: InvalidAccessError
|The autoIncrement attribute of the optionalParameters object is true; however, the keyPath attribute either an empty string ("") or an empty array.
|}
 
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/indexedDB/IDBDatabase|IDBDatabase]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}