{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Returns a long value that uniquely identifies a watch operation and then asynchronously starts the watch operation.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=successCallback
|Data type=any
|Description=The function to call when geographic position is successfully obtained. The function specified by the ''successCallback'' parameter takes one ''position'' parameter.
|Optional=No
}}{{Method Parameter
|Name=errorCallback
|Data type=any
|Description=The function to call when the attempt to obtain geographic position fails. The function specified by the ''errorCallback'' parameter takes one ''positionError'' parameter. To use the ''options'' parameter without using the ''errorCallback'' parameter, specify a '''null''' value for the ''errorCallback'' parameter.
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
|Javascript_data_type=unsigned long
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=The function begins acquiring the geographic position and returns immediately. When the position is successfully obtained, the callback function provided in the ''successCallback'' parameter is called. The parameter to the ''successCallback'' function is a '''position''' object that contains the data on the current geographic location.
If the attempt to obtain the user's location fails, the callback function that can be provided as an optional second parameter is called. The error parameter to the  ''errorCallback'' function is a '''positionError''' object that contains an error code indicating the reason for failure.

'''Note:'''  The first time a document calls the '''watchPosition''' function, the client requests permission to access the geographic location of the browser, unless the user has previously chosen to always allow or always deny permission for the website to determine location.  If the user denies permission, the function declared by the ''errorCallback'' is called and the code attribute of the error parameter of that function is set to PositionError.PERMISSION_DENIED.
Support for the attributes of the ''options'' parameter depends on the location provider available to the device running the client.  There is no guarantee that changing the properties of these attributes will affect the results reported by the location provider.
Windows Internet Explorer 9.  This property is supported only for webpages displayed in IE9 Standards mode.  For more information, please see Defining Document Compatibility.
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