{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns the gathering state of the ICE agent.}}
{{API_Object_Property
|Property_applies_to=apis/webrtc/RTCPeerConnection
|Read_only=Yes
|Javascript_data_type=RTCGatheringState
|Return_value_description=The RTCGatherState enum has the following values:
* new - The object was just created, and no networking has occurred yet.
* gathering - The ICE engine is in the process of gathering candidates for this RTCPeerConnection.
* complete - The ICE engine has completed gathering.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Events such as adding a new interface or new TURN server could cause the state to go back to gathering.
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