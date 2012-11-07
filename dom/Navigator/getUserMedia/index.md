{{Page_Title}}
{{Flags
|High-level issues=Stub
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Prompts the user for permission to use a media device such as a camera or microphone. If the user provides permission, the <code>successCallback</code> is invoked on the calling application with a [[apis/webrtc/objects/LocalMediaStream|LocalMediaStream]] object as its argument.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=constraints
|Data type=MediaStreamConstraints
|Description=The constraints parameter is a MediaStreamConstraints object with two Boolean members: video and audio. These describe the media types supporting the [[apis/webrtc/objects/LocalMediaStream|LocalMediaStream]] object. Either or both must be specified to validate the constraint argument. If a specified constraint is not supported by the browser, getUserMedia invokes the errorCallback with the NOT_SUPPORTED_ERROR. If the browser cannot find any media track with the specified type, getUserMedia invokes the errorCallback with the MANDATORY_UNSATISFIED_ERR.

If the value or the member is not specified in the object, the value for the member defaults to false. The following demonstrates how to set the constraints for both audio and video:

 { video: true, audio: true }
|Optional=No
}}{{Method Parameter
|Name=successCallback
|Data type=function
|Description=The getUserMedia function will call the function specified in the successCallback with the LocalMediaStream object that contains the media stream. You may assign that object to the appropriate element and work with it, as shown in the following example:

 function(localMediaStream) {
    var video = document.querySelector('video');
    video.src = window.URL.createObjectURL(localMediaStream);
    video.onloadedmetadata = function(e) {
       // Do something with the video here.
    };
 },
|Optional=No
}}{{Method Parameter
|Name=errorCallback
|Data type=function
|Description=The getUserMedia function will call the function specified in the errorCallback with a code argument. The error codes are described as follows:

* PERMISSION_DENIED - The user denied permission to use a media device required for the operation.
* NOT_SUPPORTED_ERROR - A constraint specified is not supported by the browser. 
* MANDATORY_UNSATISFIED_ERROR - No media tracks of the type specified in the constraints are found.
|Optional=Yes
}}
|Method_applies_to=dom/navigator
|Example_object_name=navigator
|Return_value_name=stream
|Javascript_data_type=LocalMediaStream
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Here's an example of using getUserMedia() with browser prefixes.
|Code=navigator.getMedia = ( navigator.getUserMedia
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table
|Page=apis/webrtc/objects/MediaStream
}}
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Firefox
|Version=18
|Note=Enabling WebRTC in Firefox Nightly requires you to set a flag in the configuration: *  Type "about:config" in the address bar and say yes that you want to make changes. *  Find the "media.navigator.enabled" entry and set it to true.
}}
}}
{{See_Also_Section}}
{{Topics|DOM, WebRTC}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}