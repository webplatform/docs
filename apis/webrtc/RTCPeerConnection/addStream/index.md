---
title: addStream
notes:
  - 'Needs spec reference'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webrtc/RTCPeerConnection
    href: /apis/webrtc/RTCPeerConnection
summary: 'Adds a new stream to the RTCPeerConnection.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebRTC
uri: apis/webrtc/RTCPeerConnection/addStream

---
## <span>Summary</span>

Adds a new stream to the RTCPeerConnection.

Method of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## <span>Syntax</span>

``` js
 element.addStream();
```

## <span>Return Value</span>

No return value

## <span>Examples</span>

``` js
/*
 * This examples assumes that the browser supports WebRTC API and
 * attaches to the peerconnection the stream that gets from the
 * user's media interfaces
 */

var connection, constraints, peerconnection; // Peerconnection related
var success, error; //Callback functions

connection = { iceServers: [{url: '...', credential: '...'} ,{...}] };
constraints = { optional: [...] };
peerconnection = RTCPeerConnection(connection, constraints);

success = function(stream){
  //Attach the stream to the connection.
  //Sidenote: This will trigger 'negotiationneeded' event
  peerconnection.addStream(stream);
};

error = function(err){
  console.log(err);
};

navigator.getUserMedia({audio: true, video: true}, success, error);
```

## <span>Usage</span>

     If the RTCPeerConnection object's readyState is closed, throws an INVALID_STATE exception.

Otherwise, destroys the ICE agent, abruptly ending any active ICE processing, any active streaming, and releasing any relevant resources (e.g. TURN permissions); then sets the [readyState](/apis/webrtc/RTCPeerConnection/readyState) to `closed`.