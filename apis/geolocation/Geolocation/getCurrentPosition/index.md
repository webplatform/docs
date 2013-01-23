{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Obtains the current location of the device.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=successCallback
|Data type=any
|Description=The function to call when geographic position is successfully obtained. The function specified by the ''successCallback'' parameter takes one ''position'' parameter.
|Optional=No
}}{{Method Parameter
|Name=errorCallback
|Data type=any
|Description=The function to call when the method fails. The function specified by the ''errorCallback'' parameter takes one ''positionError'' parameter. 
To use the ''options'' parameter without using the ''errorCallback''  parameter, set the ''errorCallback'' parameter to '''null'''.
|Optional=Yes
}}{{Method Parameter
|Name=options
|Data type=any
|Description=JSON encoding
|Optional=Yes
}}
|Method_applies_to=apis/geolocation/Geolocation
|Example_object_name=Geolocation
|Return_value_name=object
|Javascript_data_type=void
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=Windows Internet Explorer 9.  This property is supported only for webpages displayed in IE9 Standards mode.  For more information, see Defining Document Compatibility.
When the '''getCurrentPosition''' function is called, it initiates a request to acquire the geographic position, and then returns immediately.  If the geographic position is successfully obtained, the callback function defined in the ''successCallback'' parameter is called. The ''position'' parameter of that function contains the data describing the current geographic location of the device running Internet Explorer.
If the geographic location cannot be obtained and a callback function is specified as the ''errorCallback'' parameter, that function is called.  The error parameter of the ''errorCallback'' function contains an error code indicating the reason for failure.
'''Note:'''  The first time a web application calls the '''getCurrentPosition''' function, Internet Explorer requests permission to access the geographic location of the browser, unless the user has previously chosen to always allow or always deny permission for the website to determine location.  If the user denies permission, the function declared by the ''errorCallback'' is called, and the code attribute of the error parameter of that function is set to PositionError.PERMISSION_DENIED.
Support for the attributes of the ''options'' parameter depends on the location provider available to the device running Internet Explorer.  There is no guarantee that changing the properties of these attributes will affect the results reported by the location provider.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Geolocation Specification
|URL=http://dev.w3.org/geo/api/spec-source.html
|Status=W3C Proposed Recommendation
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
{{Topics|Geolocation}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}