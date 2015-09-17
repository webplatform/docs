---
title: 'addIceCandidate'
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webrtc/RTCPeerConnection
    href: /apis/webrtc/RTCPeerConnection
standardization_status: 'W3C Working Draft'
summary: 'Provides a remote candidate to the ICE agent.'
tags:
  - API_Object_Methods
  - API
  - WebRTC
  - Needs_Examples
uri: apis/webrtc/RTCPeerConnection/addIceCandidate

---
## Summary

Provides a remote candidate to the ICE agent.

Method of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## Syntax

``` js
 element.addIceCandidate(candidate);
```

## Parameters

### candidate

 Data-type
:   RTCIceCandidate

 See [RTCIceCandidate](/apis/webrtc/RTCIceCandidate).

## Return Value

No return value

## Usage

     An exception with an RTCError object of type INVALID_CANDIDATE_TYPE is thrown if candidate parameter is malformed.

## Notes

In addition to being added to the remote description, connectivity checks will be sent to the new candidates as long as the `IceTransports` constraint is not set to `none`. This call will result in a change to the state of the ICE Agent, and may result in a change to media state if it results in different connectivity being established.
