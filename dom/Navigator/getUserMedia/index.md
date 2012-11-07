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
}}
|Method_applies_to=dom/navigator
|Example_object_name=navigator
|Return_value_name=stream
|Javascript_data_type=LocalMediaStream
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}