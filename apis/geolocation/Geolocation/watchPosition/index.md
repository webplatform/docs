{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=successCallback|Data type=IDispatch|Description=The function to call when geographic position is successfully obtained. The function specified by the ''successCallback'' parameter takes one [[apis/geolocation/objects/position|'''position''']] parameter.|Optional=}}
{{Method Parameter|Name=errorCallback|Data type=IDispatch|Description=The function to call when the attempt to obtain geographic position fails. The function specified by the ''errorCallback'' parameter takes one [[apis/geolocation/objects/positionError|'''positionError''']] parameter. To use the ''options'' parameter without using the ''errorCallback'' parameter, specify a '''null''' value for the ''errorCallback'' parameter.|Optional=}}
{{Method Parameter|Name=options|Data type=IDispatch|Description=JSON encoding|Optional=}}
{{Method Parameter|Name=watchId|Data type=Integer|Description=An identifier representing the watch operation. This value is passed to the [[apis/geolocation/methods/clearWatch|'''clearWatch''']] function in order  to stop listening for location updates.|Optional=}}
|Method_applies_to=apis/geolocation/objects/geolocation
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

'''Integer'''

An identifier representing the watch operation. This value is passed to the [[apis/geolocation/methods/clearWatch|'''clearWatch''']] function in order  to stop listening for location updates.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
The function begins acquiring the geographic position and returns immediately. When the position is successfully obtained, the callback function provided in the ''successCallback'' parameter is called. The parameter to the ''successCallback'' function is a [[apis/geolocation/objects/position|'''position''']] object that contains the data on the current geographic location.
If the attempt to obtain the user's location fails, the callback function that can be provided as an optional second parameter is called. The error parameter to the  ''errorCallback'' function is a [[apis/geolocation/objects/positionError|'''positionError''']] object that contains an error code indicating the reason for failure.
'''Note'''  The first time a document calls the '''watchPosition''' function, the client requests permission to access the geographic location of the browser, unless the user has previously chosen to always allow or always deny permission for the website to determine location.  If the user denies permission, the function declared by the ''errorCallback'' is called and the code attribute of the error parameter of that function is set to PositionError.PERMISSION_DENIED.
Support for the attributes of the ''options'' parameter depends on the location provider available to the device running the client.  There is no guarantee that changing the properties of these attributes will affect the results reported by the location provider.
Windows Internet Explorer 9.  This property is supported only for webpages displayed in IE9 Standards mode.  For more information, please see Defining Document Compatibility.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}208506 Geolocation API Specification], Section 5.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Reference</code>
*<code>IWebGeolocation</code>
*<code>[[apis/geolocation/objects/geolocation|geolocation]]</code>
*<code>[[apis/geolocation/methods/clearWatch|clearWatch]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}