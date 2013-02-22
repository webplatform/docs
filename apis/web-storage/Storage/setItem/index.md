{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Adds or replaces a value for the given key.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=key
|Data type=String
|Description=The name of the key (a valid UTF-16 string, including the empty string).
|Optional=No
}}{{Method Parameter
|Name=value
|Data type=String
|Description=The value (a valid UTF-16 string) for the key/value pair.
|Optional=No
}}
|Method_applies_to=apis/web-storage/Storage
|Example_object_name=object
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code examples are equivalent. The first sets a key/value pair by calling '''setItem'''. The second uses array syntax to find the key in the collection. The final example uses property name syntax to set an expando property.
|Code=sessionStorage.setItem('myKey', '...');
					
sessionStorage['myKey'] {{=}} '...'; 
	
sessionStorage.myKey {{=}} '...';
}}
}}
{{Notes_Section
|Notes=Any valid UTF-16 string, including the empty string, is a valid key name. If ''key'' or ''value'' are not valid UTF-16 strings, the '''setItem''' method throws an error.
Non-string variable types are automatically type-converted to strings, if possible. Structured data must be converted to a string before storing.
This method first checks if a key/value pair with the specified ''key'' already exists in the list associated with the object. If not, a new key/value pair with the given value is added to the list. If the key/value pair already exists, the value is updated.
Keys are also available as expando properties on the '''Storage''' object. If the property name does not exist, a key/value pair is created for it.
If the size of the value is larger than the disk quota remaining for the storage area, an "Out of memory" exception is thrown.
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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=23.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
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