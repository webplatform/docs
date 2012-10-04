{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=watchId|Data type=Integer|Description=The ID of the watch operation to cancel. This value is returned by the [[apis/geolocation/methods/watchPosition|'''watchPosition''']] method.|Optional=}}
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
|Description=In the following example, the user can click the '''Watch Latitude and Longitude''' button to call the '''listenForPosition''' function in the example. The '''listenForPosition''' function confirms that the [[apis/geolocation/objects/geolocation|'''geolocation''']] object is available before calling  the [[apis/geolocation/methods/watchPosition|'''watchPosition''']] method in order to start listening for location updates. When an update occurs, the success callback function updates the text boxes in the page by using the new latitude and longitude coordinates. The user can click the '''Clear Watch''' button to call the '''clearWatch''' method and stop listening for updates. No further callbacks will be invoked after the '''clearWatch''' method is called.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt;  
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Listening for Location Updates&lt;/title&gt;
&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}9" /&gt;
&lt;script type{{=}}"text/javascript"&gt;
function setText(val, e) {
    document.getElementById(e).value {{=}} val;
}
function insertText(val, e) {
    document.getElementById(e).value +{{=}} val;
}
var nav {{=}} null; 
var watchID;
function listenForPosition() {
  if (nav {{=}}{{=}} null) {
      nav {{=}} window.navigator;
  }
  if (nav !{{=}} null) {
      var geoloc {{=}} nav.geolocation;
      if (geoloc !{{=}} null) {
          watchID {{=}} geoloc.watchPosition(successCallback, errorCallback);
      }
      else {
          console.log("Geolocation not supported");
      }
  }
  else {
      console.log("Navigator not found");
  }
}
function clearWatch(watchID) {
    window.navigator.geolocation.clearWatch(watchID);
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
    // information that helps to identify the situation so that 
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
&lt;input type{{=}}"button" onclick{{=}}"listenForPosition ()" value{{=}}"Watch Latitude and Longitude"  /&gt; 
&lt;input type{{=}}"button" value{{=}}"Clear watch" onclick{{=}}"clearWatch()" /&gt;
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
If the ''watchId'' parameter does not correspond to any watch process started by a previous call to the [[apis/geolocation/methods/watchPosition|'''watchPosition''']] method, this method returns and no further action is taken.
Windows Internet Explorer 9.  This property is supported only for webpages displayed in IE9 Standards mode.  For more information, see Defining Document Compatibility.
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
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}