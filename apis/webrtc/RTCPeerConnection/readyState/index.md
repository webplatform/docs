{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs example, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns the ready state of the peer connection.}}
{{API_Object_Property
|Property_applies_to=apis/webrtc/RTCPeerConnection
|Read_only=Yes
|Example_object_name=
|Return_value_name=
|Javascript_data_type=RTCPeerState
|Return_value_description=The RTCPeerState enum has the following values:
* new - the object was just created; no netorking has transpired
* have-local-offer - a local description of type offer has been supplied
* have-local-pranswer - a remote description of type offer has been supplied and a local description of type pranswer has been supplied
* have-remote-pranswer - a local description of type "offer" has been supplied and a remote description of type "pranswer" has been supplied
* active - both local and remote descriptions have been supplied, and the offer-answer exchange is complete 
* closed - the connection is closed
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=
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