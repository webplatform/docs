{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=watchId
|Data type=String
|Description=The ID of the watch operation to cancel. This value is returned by the [[apis/geolocation/methods/watchPosition|'''watchPosition''']] method.
|Optional=No
}}
|Method_applies_to=apis/geolocation/objects/geolocation
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In the following example, the user can click the '''Watch Latitude and Longitude''' button to call the '''listenForPosition''' function in the example. The '''listenForPosition''' function confirms that the [[apis/geolocation/objects/geolocation|'''geolocation''']] object is available before calling  the [[apis/geolocation/methods/watchPosition|'''watchPosition''']] method in order to start listening for location updates. When an update occurs, the success callback function updates the text boxes in the page by using the new latitude and longitude coordinates. The user can click the '''Clear Watch''' button to call the '''clearWatch''' method and stop listening for updates. No further callbacks will be invoked after the '''clearWatch''' method is called.
|Code=&lt;!DOCTYPE html&gt;  
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
}}
}}
{{Notes_Section
|Notes====Remarks===
If the ''watchId'' parameter does not correspond to any watch process started by a previous call to the [[apis/geolocation/methods/watchPosition|'''watchPosition''']] method, this method returns and no further action is taken.
Windows Internet Explorer 9.  This property is supported only for webpages displayed in IE9 Standards mode.  For more information, see Defining Document Compatibility.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}208506 Geolocation API Specification], Section 5.1
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=14.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.0
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>IWebGeolocation</code>
*<code>[[apis/geolocation/objects/geolocation|geolocation]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}