{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the current value associated with the given key.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=key
|Data type=String
|Description=The name of the key (a valid UTF-16 string, including the empty string).
|Optional=No
}}
|Method_applies_to=apis/web-storage/Storage
|Example_object_name=object
|Javascript_data_type=String
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Any valid UTF-16 string, including the empty string, is a valid key name.
If the specified ''key'' does not exist in the list associated with the object, then this method returns '''null'''.
Attempts to read or write a secured item from script running in the context of an unsecured URL are not permitted.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Web Storage Specification
|URL=http://dev.w3.org/html5/webstorage
|Status=W3C Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Webstorage}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}