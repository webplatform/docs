---
title: 'remoteStreams'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webrtc/RTCPeerConnection
    href: /apis/webrtc/RTCPeerConnection
standardization_status: 'W3C Working Draft'
summary: 'Returns an array of MediaStream objects added to the connection by the remote peer. This array is updated when the addstream and removestream events are fired.'
tags:
  - API_Object_Properties
  - API
  - WebRTC
  - Needs_Examples
uri: apis/webrtc/RTCPeerConnection/remoteStreams

---
## Summary

Returns an array of MediaStream objects added to the connection by the remote peer. This array is updated when the addstream and removestream events are fired.

Property of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.remoteStreams;
```

