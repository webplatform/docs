---
title: iceGatheringState
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example, spec reference'
summary: 'Returns the gathering state of the ICE agent.'
uri: apis/webrtc/RTCPeerConnection/iceGatheringState

---
# iceGatheringState

## Summary

Returns the gathering state of the ICE agent.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.iceGatheringState;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">RTCGatheringState</span></span>

The RTCGatherState enum has the following values:

-   new - The object was just created, and no networking has occurred yet.
-   gathering - The ICE engine is in the process of gathering candidates for this RTCPeerConnection.
-   complete - The ICE engine has completed gathering.

**Needs Examples**: This section should include examples.

## Notes

Events such as adding a new interface or new TURN server could cause the state to go back to gathering.

