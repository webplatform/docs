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