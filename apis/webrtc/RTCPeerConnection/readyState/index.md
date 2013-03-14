{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns the ready state of the peer connection.}}
{{API_Object_Property
|Property_applies_to=apis/webrtc/RTCPeerConnection
|Read_only=Yes
|Javascript_data_type=RTCPeerState
|Return_value_description=The RTCPeerState enum has the following values:
* new - the object was just created; no netorking has transpired
* have-local-offer - a local description of type offer has been supplied
* have-local-pranswer - a remote description of type offer has been supplied and a local description of type pranswer has been supplied
* have-remote-pranswer - a local description of type "offer" has been supplied and a remote description of type "pranswer" has been supplied
* active - both local and remote descriptions have been supplied, and the offer-answer exchange is complete 
* closed - the connection is closed
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