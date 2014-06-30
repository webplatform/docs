{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs example, spec reference, return value
|Checked_Out=No
|High-level issues=Needs Review
|Content=Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Creates a session description compatible with the remote configuration.}}
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
|Usage=Generates an SDP answer with the supported configuration for the session that is compatible with the parameters in the remote configuration. Like createOffer, the returned blob contains descriptions of the local MediaStreams attached to this RTCPeerConnection, the codec/RTP/RTCP options negotiated for this session, and any candidates that have been gathered by the ICE Agent. The constraints parameter may be supplied to provide additional control over the generated answer.
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