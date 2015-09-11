---
title: createAnswer
notes:
  - 'Needs example, spec reference, return value'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webrtc/RTCPeerConnection
    href: /apis/webrtc/RTCPeerConnection
standardization_status: 'W3C Working Draft'
summary: 'Creates a session description compatible with the remote configuration.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebRTC
uri: apis/webrtc/RTCPeerConnection/createAnswer

---
## <span>Summary</span>

Creates a session description compatible with the remote configuration.

Method of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## <span>Syntax</span>

``` js
 element.createAnswer();
```

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Usage</span>

     Generates an SDP answer with the supported configuration for the session that is compatible with the parameters in the remote configuration. Like createOffer, the returned blob contains descriptions of the local MediaStreams attached to this RTCPeerConnection, the codec/RTP/RTCP options negotiated for this session, and any candidates that have been gathered by the ICE Agent. The constraints parameter may be supplied to provide additional control over the generated answer.