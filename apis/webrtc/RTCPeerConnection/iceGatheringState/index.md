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
## <span>Summary</span>

Returns the gathering state of the ICE agent.

Property of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.iceGatheringState;
```

## <span>Return Value</span>

Returns an object of type RTCGatheringStateRTCGatheringState

The RTCGatherState enum has the following values:

-   new - The object was just created, and no networking has occurred yet.
-   gathering - The ICE engine is in the process of gathering candidates for this RTCPeerConnection.
-   complete - The ICE engine has completed gathering.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

Events such as adding a new interface or new TURN server could cause the state to go back to gathering.