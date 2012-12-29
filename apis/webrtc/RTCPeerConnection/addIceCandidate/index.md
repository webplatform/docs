{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Provides a remote candidate to the ICE agent.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=candidate
|Data type=RTCIceCandidate
|Description=See [[apis/webrtc/RTCIceCandidate|RTCIceCandidate]].
|Optional=No
}}
|Method_applies_to=apis/webrtc/RTCPeerConnection
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=An exception with an <code>RTCError</code> object of type <code>INVALID_CANDIDATE_TYPE</code> is thrown if candidate parameter is malformed.
|Notes=In addition to being added to the remote description, connectivity checks will be sent to the new candidates as long as the <code>IceTransports</code> constraint is not set to <code>none</code>. This call will result in a change to the state of the ICE Agent, and may result in a change to media state if it results in different connectivity being established.
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
{{Topics|WebRTC}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}