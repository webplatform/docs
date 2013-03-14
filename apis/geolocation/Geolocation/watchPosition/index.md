{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
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
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Obtains users position and position changes for 120s.
|Code=var watchID;
var geoLoc;

function showLocation(position) 
{  
alert('latitude: '+position.coords.latitude+' AND longitude: '+position.coords.longitude);
}

function errorHandler(err) {
  if(err.code == 1) {
    alert("Error: Access is denied!");
  }else if( err.code == 2) {
    alert("Error: Position is unavailable!");
  }
}
function getLocationUpdate(){

   if(navigator.geolocation){
      // timeout at 120000 milliseconds (120 seconds)
      var options = {timeout:120000};
      geoLoc = navigator.geolocation;
      watchID = geoLoc.watchPosition(showLocation, 
                                     errorHandler,
                                     options);
   }else{
      alert("Sorry, browser does not support geolocation!");
   }
}
getLocationUpdate();
}}
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
|Internet_explorer_version=9.0
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
{{Topics|API, Geolocation}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Using_geolocation
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}