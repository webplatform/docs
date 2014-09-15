{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs example, spec reference
|Checked_Out=No
|High-level issues=Stub, Missing Relevant Sections, Needs Review
|Content=Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Handles the [[apis/webrtc/RTCPeerConnection/addstream|addstream]] event fired when [[apis/webrtc/RTCPeerConnection/setRemoteDescription|setRemoteDescription()]] is called.}}
{{API_Object_Property
|Property_applies_to=apis/webrtc/RTCPeerConnection
|Read_only=No
|Example_object_name=
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=This is called any time a MediaStream is added by the remote peer. This will be fired only as a result of [[apis/webrtc/RTCPeerConnection/setRemoteDescription|setRemoteDescription()]]. The onnaddstream callback happens as early as possible after  setRemoteDescription(), it does not wait for a given media stream to be accepted or rejected via SDP negotiation.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, WebRTC}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}