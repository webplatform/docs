{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=successCallback|Data type=IDispatch|Description=The handler function to call when geographic position is successfully obtained. The function specified by the ''successCallback'' parameter takes one [[apis/geolocation/objects/position|'''position''']] parameter.|Optional=}}
{{Method Parameter|Name=errorCallback|Data type=IDispatch|Description=The handler function to call when the attempt to obtain geographic position fails. The function specified by the ''errorCallback'' parameter takes one [[apis/geolocation/objects/positionError|'''positionError''']] parameter. 
To use the ''options'' parameter without using the ''errorCallback''  parameter, set the ''errorCallback'' parameter to '''null'''.|Optional=}}
{{Method Parameter|Name=options|Data type=IDispatch|Description=JSON encoding|Optional=}}
|Method_applies_to=apis/geolocation/objects/geolocation
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to call the '''getCurrentPosition''' function and handle the incoming position data using callback functions. When the user clicks a button, the example ''listenForPositionUpdates'' function is called, which checks that the geolocation object is available before it calls the '''getCurrentPosition''' function. When the position is obtained, the callback function updates the text boxes in the page by using the latitude and longitude coordinates. If an error occurs while obtaining location, the error callback function displays a message based on the error object's code attribute.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt;  
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Location Test with Buttons&lt;/title&gt;
&lt;script type{{=}}"text/javascript"&gt;
function setText(val, e) {
    document.getElementById(e).value {{=}} val;
}
function insertText(val, e) {
    document.getElementById(e).value +{{=}} val;
}
var nav {{=}} null; 
function requestPosition() {
  if (nav {{=}}{{=}} null) {
      nav {{=}} window.navigator;
  }
  if (nav !{{=}} null) {
      var geoloc {{=}} nav.geolocation;
      if (geoloc !{{=}} null) {
          geoloc.getCurrentPosition(successCallback, errorCallback);
      }
      else {
          console.log("Geolocation not supported");
      }
  }
  else {
      console.log("Navigator not found");
  }
}
function successCallback(position)
{
   setText(position.coords.latitude, "latitude");
   setText(position.coords.longitude, "longitude");
}
 
function errorCallback(error) {
    var message {{=}} "";   
    // Check for known errors
    switch (error.code) {
        case error.PERMISSION_DENIED:
            message {{=}} "This website does not have permission to use " + 
                      "the Geolocation API";
            break;
        case error.POSITION_UNAVAILABLE:
            message {{=}} "The current position could not be determined.";
            break;
        case error.PERMISSION_DENIED_TIMEOUT:
            message {{=}} "The current position could not be determined " + 
                      "within the specified timeout period.";            
            break;
    }
    // If it's an unknown error, build a message that includes 
    // information that helps identify the situation, so that 
    // the error handler can be updated.
    if (message {{=}}{{=}} "")
    {
        var strErrorCode {{=}} error.code.toString();
        message {{=}} "The position could not be determined due to " + 
                  "an unknown error (Code: " + strErrorCode + ").";
    }
    console.log(message);
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;label for{{=}}"latitude"&gt;Latitude: &lt;/label&gt;&lt;input id{{=}}"latitude" /&gt; &lt;br /&gt;
&lt;label for{{=}}"longitude"&gt;Longitude: &lt;/label&gt;&lt;input id{{=}}"longitude" /&gt; &lt;br /&gt;
&lt;input type{{=}}"button" onclick{{=}}"requestPosition()" value{{=}}"Get Latitude and Longitude"  /&gt; 
&lt;/body&gt;
&lt;/html&gt;

}}}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 9.  This property is supported only for webpages displayed in IE9 Standards mode.  For more information, see Defining Document Compatibility.
When the '''getCurrentPosition''' function is called, it initiates a request to acquire the geographic position, and then returns immediately.  If the geographic position is successfully obtained, the callback function defined in the ''successCallback'' parameter is called. Te [[apis/geolocation/objects/position|'''position''']] parameter of that function contains the data describing the current geographic location of the device running Internet Explorer.
If the geographic location cannot be obtained and a callback function is specified as the ''errorCallback'' parameter, that function is called.  The error parameter of the ''errorCallback'' function contains an error code indicating the reason for failure.
'''Note'''  The first time a web application calls the '''getCurrentPosition''' function, Internet Explorer requests permission to access the geographic location of the browser, unless the user has previously chosen to always allow or always deny permission for the website to determine location.  If the user denies permission, the function declared by the ''errorCallback'' is called, and the code attribute of the error parameter of that function is set to PositionError.PERMISSION_DENIED.
Support for the attributes of the ''options'' parameter depends on the location provider available to the device running Internet Explorer.  There is no guarantee that changing the properties of these attributes will affect the results reported by the location provider.
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
*<code>[[apis/geolocation/objects/positionError|positionError]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}