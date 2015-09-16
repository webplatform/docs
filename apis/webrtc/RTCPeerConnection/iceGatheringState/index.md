---
title: iceGatheringState
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webrtc/RTCPeerConnection
    href: /apis/webrtc/RTCPeerConnection
  return:
    predicate: 'Returns an object of type '
    value: RTCGatheringState
    href: /apis/webrtc/RTCPeerConnection
standardization_status: 'W3C Working Draft'
summary: 'Returns the gathering state of the ICE agent.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
uri: apis/webrtc/RTCPeerConnection/iceGatheringState

---
## Summary

Returns the gathering state of the ICE agent.

Property of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.iceGatheringState;
```

## Return Value

Returns an object of type RTCGatheringStateRTCGatheringState

The RTCGatherState enum has the following values:

-   new - The object was just created, and no networking has occurred yet.
-   gathering - The ICE engine is in the process of gathering candidates for this RTCPeerConnection.
-   complete - The ICE engine has completed gathering.

**Needs Examples**: This section should include examples.

## Notes

Events such as adding a new interface or new TURN server could cause the state to go back to gathering.
