---
title: createAnswer
tags:
  0: API
  1: Object
  2: Methods
  4: WebRTC
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example, spec reference, return value'
summary: 'Creates a session description compatible with the remote configuration.'
uri: apis/webrtc/RTCPeerConnection/createAnswer

---
# createAnswer

## Summary

Creates a session description compatible with the remote configuration.

*Method of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)*

## Syntax

``` {.js}
 element.createAnswer();
```

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Usage

     Generates an SDP answer with the supported configuration for the session that is compatible with the parameters in the remote configuration. Like createOffer, the returned blob contains descriptions of the local MediaStreams attached to this RTCPeerConnection, the codec/RTP/RTCP options negotiated for this session, and any candidates that have been gathered by the ICE Agent. The constraints parameter may be supplied to provide additional control over the generated answer.

