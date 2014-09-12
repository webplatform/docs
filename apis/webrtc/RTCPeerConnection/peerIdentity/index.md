{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs example, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Contains the peer identity assertion information if an identity assertion was provided and verified.}}
{{API_Object_Property
|Property_applies_to=apis/webrtc/RTCPeerConnection
|Read_only=Yes
|Example_object_name=
|Return_value_name=
|Javascript_data_type=RTCIdentityAssertion
|Return_value_description=The RTCIdentityAssertion object has two string members:
* idp - the domain name representing the identity provider
* name - the name of the verified peer identity
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example shows how to consume identity assertions.
|Code=pc.onidentityresult = function(result) {
  console.log("IdP= " + pc.peerIdentity.idp +
              " identity=" + pc.peerIdentity.name);
};
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=The identity system is designed so that applications need not take any special action in order for users to generate and verify identity assertions; if a user has configured an IdP into their browser, then the browser will automatically request/generate assertions and the other side will automatically verify them and display the results.
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