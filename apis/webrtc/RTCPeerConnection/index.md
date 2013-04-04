{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Provides for the connection between remote peers, the transmission of locally generated MediaStream data and arbitrary data between peers.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Code=/*
 * This examples assumes that the browser supports WebRTC API and
 * attaches to the peerconnection the stream that gets from the 
 * user's media interfaces
 */

var connection, constraints, peerconnection; // Peerconnection related
var success, error; //Callback functions

connection = {'iceServers': [ {'url': '...', 'credential': [...]} ,{...} ]};
constraints = { optional: [...] };
peerconnection = RTCPeerConnection(connection, constraints);

success = function(stream){
  peerconnection.addStream(stream);
};

error = function(err){
  console.log(err);
};

navigator.getUserMedia({audio: true, video: true}, success, error);
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
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