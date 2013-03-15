{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Adds a new stream to the RTCPeerConnection.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/webrtc/RTCPeerConnection
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=If the RTCPeerConnection object's [[apis/webrtc/RTCPeerConnection/readyState|readyState]] is <code>closed</code>, throws an <code>INVALID_STATE</code> exception.
Otherwise, destroys the ICE agent, abruptly ending any active ICE processing, any active streaming, and releasing any relevant resources (e.g. TURN permissions); then sets the [[apis/webrtc/RTCPeerConnection/readyState|readyState]] to <code>closed</code>.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|API, WebRTC}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}