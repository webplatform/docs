{{Page_Title|Geolocation}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The Geolocation object is used by scripts to programmatically determine the location information associated with the hosting device. The location information is acquired by applying a user-agent specific algorithm, creating a '''Position''' object, and populating that object with appropriate data accordingly.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The geolocation API is published through a geolocation child object within the navigator object.  If the object exists, geolocation services are available.
|Code=if ("geolocation" in navigator) {
  /* geolocation is available */
  alert("Geolocation services are supported by your browser.");
} else {
 /* geolocation is not available */ 
  alert("I'm sorry, but geolocation services are not supported by your browser.");
}
}}{{Single Example
|Language=JavaScript
|Description=The script checks if geolocation is supported, if possible - the script obtains your actual position using the watchPosition method.
If something went wrong you will get a detailed error message.
|Code=// variables	  
var watchID;
var geoLoc;

// check if geolocation is available
if ("geolocation" in navigator) 
{
/* geolocation is available */
	alert("Geolocation services are supported by your browser.");
	getLocationUpdate();
} 

else 
{
/* geolocation is not available */ 
	alert("I'm sorry, but geolocation services are not supported by your browser.");
}	  

function showLocation(position) 
{  
alert('latitude: '+position.coords.latitude+' AND longitude: '+position.coords.longitude);
alert(position.coords.accuracy);
}

function errorHandler(err)
{ 
if(err.code == 0) 
{alert("Error: Unknown error");}

else if( err.code == 1) 
{alert("Error: Permission denied");}

else if( err.code == 2) 
{alert("Error: Position not available");}

else if( err.code == 3) 
{alert("Error: Timeout");}

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
}}
}}
{{Notes_Section
|Notes=Windows Internet Explorer 9.  The '''Geolocation''' object is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility.
The '''Geolocation''' object is not supported for applications hosting the WebBrowser Control.
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
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}