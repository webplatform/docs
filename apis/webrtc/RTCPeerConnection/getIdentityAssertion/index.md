{{Page_Title}}
{{Flags
|High-level issues=Stub, Missing Relevant Sections, Needs Review
|Content=Incomplete
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Provides an identity assertion.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/webrtc/RTCPeerConnection
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Applications need not make this call. It is merely intended to allow them to start the process of obtaining identity assertions before a call is initiated. If an identity is needed, either because the browser has been configured with a default identity provider or because the [[apis/webrtc/RTCPeerConnection/setIdentityProvider|setIdentityProvider()]] method was called, then an identity will be automatically requested when an offer or answer is created.
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