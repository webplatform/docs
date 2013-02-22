{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the name of the '''n'''th key in the list.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=index
|Data type=unsigned long
|Description=A zero-based index of the list entry, up to the length of the collection.
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
|Notes=The returned key can be any string, including the empty string.
The order of keys may change when items are added to the collection.
This method will throw an "Invalid Argument" exception if ''index'' is out of range.
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