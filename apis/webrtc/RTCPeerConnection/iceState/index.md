{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns the ICE state of the ICE agent.}}
{{API_Object_Property
|Property_applies_to=apis/webrtc/RTCPeerConnection
|Read_only=Yes
|Javascript_data_type=RTCIceState
|Return_value_description=The RTCIceState enum has the following values:
* starting - The ICE Agent is gathering addresses and/or waiting for remote candidates to be supplied.
* checking - The ICE Agent has received remote candidates on at least one component, and is checking candidate pairs but has not yet found a connection. In addition to checking, it may also still be gathering.
* connected - The ICE Agent has found a usable connection for all components but is still checking other candidate pairs to see if there is a better connection. It may also still be gathering.
* completed - The ICE Agent has finished gathering and checking and found a connection for all components.
* failed - The ICE Agent is finished checking all candidate pairs and failed to find a connection for at least one component.
* disconnected - Liveness checks have failed for one or more components. This is more aggressive than failed, and may trigger intermittently (and resolve itself without action) on a flaky network.
* closed - The ICE Agent has shut down and is no longer responding to STUN requests.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=An example transition might look like this:
* new PeerConnection(): Starting
* (Starting, remote candidates received): Checking
* (Checking, found usable connection): Connected
* (Checking, gave up): Failed
* (Connected, finished all checks): Completed
* (Completed, lost connectivity): Disconnected
* (any state, ICE restart occurs): Starting
* close(): Closed
|Notes=States take either the value of any component or all components, as outlined here:
* <code>checking</code> occurs if ANY component has received a candidate and can start checking.
* <code>connected</code> occurs if ALL components have established a working connection.
* <code>completed</code> occurs if ALL components have finalized the running of their ICE processes.
* <code>failed</code> occurs if ANY component has given up trying to connect.
* <code>disconnected</code> occurs if ANY component has failed liveness checks.
* <code>closed</code> occurs only if PeerConnection.close() has been called.
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