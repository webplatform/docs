{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns the current state of the XHR.}}
{{API_Object_Property
|Property_applies_to=apis/xhr/XMLHttpRequest
|Read_only=Yes
|Javascript_data_type=unsigned short
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=You cannot call the '''responseText''' property to obtain partial results ('''readyState''' {{=}} 3). Doing so will return an error, because the response is not fully received. You must wait until all data has been received.
See [[apis/xhr/XMLHttpRequest/readystatechange|'''onreadystatechange''']].

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