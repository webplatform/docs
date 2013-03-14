{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Contains the peer identity assertion information if an identity assertion was provided and verified.}}
{{API_Object_Property
|Property_applies_to=apis/webrtc/RTCPeerConnection
|Read_only=Yes
|Javascript_data_type=RTCIdentityAssertion
|Return_value_description=The RTCIdentityAssertion object has two string members:
* idp - the domain name representing the identity provider
* name - the name of the verified peer identity
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
}}
}}
{{Notes_Section
|Notes=The identity system is designed so that applications need not take any special action in order for users to generate and verify identity assertions; if a user has configured an IdP into their browser, then the browser will automatically request/generate assertions and the other side will automatically verify them and display the results.
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