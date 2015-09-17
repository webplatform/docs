---
title: 'localDescription'
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
    value: RTCSessionDescription
    href: /apis/webrtc/RTCPeerConnection
standardization_status: 'W3C Working Draft'
summary: 'Returns the RTCSessionDescription most recently passed to the setLocalDescription() method along with any local candidate descriptions generated since the method was called.'
tags:
  - API_Object_Properties
  - API
  - WebRTC
  - Needs_Examples
uri: apis/webrtc/RTCPeerConnection/localDescription

---
## Summary

Returns the RTCSessionDescription most recently passed to the setLocalDescription() method along with any local candidate descriptions generated since the method was called.

Property of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.localDescription;
```

## Return Value

Returns an object of type RTCSessionDescriptionRTCSessionDescription

Returns a null object if the local description has not yet been set.

