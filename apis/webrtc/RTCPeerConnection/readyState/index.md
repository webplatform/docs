---
title: readyState
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Returns the ready state of the peer connection.'
uri: apis/webrtc/RTCPeerConnection/readyState

---
# readyState

## Summary

Returns the ready state of the peer connection.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.readyState;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">RTCPeerState</span></span>

The RTCPeerState enum has the following values:

-   new - the object was just created; no netorking has transpired
-   have-local-offer - a local description of type offer has been supplied
-   have-local-pranswer - a remote description of type offer has been supplied and a local description of type pranswer has been supplied
-   have-remote-pranswer - a local description of type "offer" has been supplied and a remote description of type "pranswer" has been supplied
-   active - both local and remote descriptions have been supplied, and the offer-answer exchange is complete
-   closed - the connection is closed

**Needs Examples**: This section should include examples.

