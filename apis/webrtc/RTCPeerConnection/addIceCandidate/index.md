---
title: addIceCandidate
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
  0: API
  1: Object
  2: Methods
  4: WebRTC
uri: apis/webrtc/RTCPeerConnection/addIceCandidate

---
## <span>Summary</span>

Provides a remote candidate to the ICE agent.

Method of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## <span>Syntax</span>

``` js
 element.addIceCandidate(candidate);
```

## <span>Parameters</span>

### <span>candidate</span>

 Data-type
:   RTCIceCandidate

 See [RTCIceCandidate](/apis/webrtc/RTCIceCandidate).

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Usage</span>

     An exception with an RTCError object of type INVALID_CANDIDATE_TYPE is thrown if candidate parameter is malformed.

## <span>Notes</span>

In addition to being added to the remote description, connectivity checks will be sent to the new candidates as long as the `IceTransports` constraint is not set to `none`. This call will result in a change to the state of the ICE Agent, and may result in a change to media state if it results in different connectivity being established.