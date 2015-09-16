---
title: readyState
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webrtc/RTCPeerConnection
    href: /apis/webrtc/RTCPeerConnection
  return:
    predicate: 'Returns an object of type '
    value: RTCPeerState
    href: /apis/webrtc/RTCPeerConnection
standardization_status: 'W3C Working Draft'
summary: 'Returns the ready state of the peer connection.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
uri: apis/webrtc/RTCPeerConnection/readyState

---
## Summary

Returns the ready state of the peer connection.

Property of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.readyState;
```

## Return Value

Returns an object of type RTCPeerStateRTCPeerState

The RTCPeerState enum has the following values:

-   new - the object was just created; no netorking has transpired
-   have-local-offer - a local description of type offer has been supplied
-   have-local-pranswer - a remote description of type offer has been supplied and a local description of type pranswer has been supplied
-   have-remote-pranswer - a local description of type "offer" has been supplied and a remote description of type "pranswer" has been supplied
-   active - both local and remote descriptions have been supplied, and the offer-answer exchange is complete
-   closed - the connection is closed

**Needs Examples**: This section should include examples.

