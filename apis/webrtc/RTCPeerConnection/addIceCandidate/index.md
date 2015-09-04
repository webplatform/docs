---
title: addIceCandidate
tags:
  0: API
  1: Object
  2: Methods
  4: WebRTC
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example, spec reference'
summary: 'Provides a remote candidate to the ICE agent.'
uri: apis/webrtc/RTCPeerConnection/addIceCandidate

---
# addIceCandidate

## Summary

Provides a remote candidate to the ICE agent.

*Method of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)*

## Syntax

``` {.js}
 element.addIceCandidate(candidate);
```

## Parameters

### candidate

 Data-typeÂ
:   RTCIceCandidate

 See [RTCIceCandidate](/apis/webrtc/RTCIceCandidate).

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Usage

     An exception with an RTCError object of type INVALID_CANDIDATE_TYPE is thrown if candidate parameter is malformed.

## Notes

In addition to being added to the remote description, connectivity checks will be sent to the new candidates as long as the `IceTransports` constraint is not set to `none`. This call will result in a change to the state of the ICE Agent, and may result in a change to media state if it results in different connectivity being established.

