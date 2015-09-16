---
title: remoteDescription
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webrtc/RTCPeerConnection
    href: /apis/webrtc/RTCPeerConnection
  return:
    predicate: 'Returns an object of type '
    value: RTCSessionDescription
    href: /apis/webrtc/RTCPeerConnection
standardization_status: 'W3C Working Draft'
summary: 'Returns the RTCSessionDescription most recently passed to the setRemoteDescription() method along with any remote candidate descriptions supplied with addIceCandidate(). Returns null if the remote description has not been set.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
uri: apis/webrtc/RTCPeerConnection/remoteDescription

---
## Summary

Returns the RTCSessionDescription most recently passed to the setRemoteDescription() method along with any remote candidate descriptions supplied with addIceCandidate(). Returns null if the remote description has not been set.

Property of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.remoteDescription;
```

## Return Value

Returns an object of type RTCSessionDescriptionRTCSessionDescription

**Needs Examples**: This section should include examples.

