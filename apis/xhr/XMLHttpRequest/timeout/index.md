{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns or sets the number of milliseconds a request can take before automatically being terminated.}}
{{API_Object_Property
|Property_applies_to=apis/xhr/XMLHttpRequest
|Read_only=No
|Javascript_data_type=unsigned long
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=The '''timeout''' property has
a default value of 0.
If the time-out period expires, the
'''responseText''' property will be
null.
You should set a time-out value that is slightly longer than
the expected response time of the request.
The '''timeout''' property
may be set only in the time interval between a call to the
'''open''' method and the
first call to the '''send''' method.
If you set an '''XMLHttpRequest''' time-out value 
that is larger than the network stack's time-out value, the network stack
will time out first and the '''ontimeout''' 
event will not be raised.
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