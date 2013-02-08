{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Sets the value of an XMLHttpRequest header.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=header
|Data type=String
|Description=Specifies the header name.
|Optional=No
}}{{Method Parameter
|Name=value
|Data type=String
|Description=Specifies the header value.
|Optional=No
}}
|Method_applies_to=apis/xhr/XMLHttpRequest
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Usage=If used, must be called after open(), but before send().
|Notes=Refer to [http://go.microsoft.com/fwlink/p/?linkid{{=}}203727 RFC2616, Section 14: Header Field Definitions] for a general list of standard headers. The server is ultimately responsible for honoring the headers of the request. By far the most common request header is Content-Type, which is required by some XML Web services.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C XMLHttpRequest Specification
|URL=http://www.w3.org/TR/XMLHttpRequest/
|Status=W3C Working Draft
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
{{Topics|XHR}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}