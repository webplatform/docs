---
title: localDescription
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
  0: API
  1: Object
  2: Properties
  4: WebRTC
uri: apis/webrtc/RTCPeerConnection/localDescription

---
## <span>Summary</span>

Returns the RTCSessionDescription most recently passed to the setLocalDescription() method along with any local candidate descriptions generated since the method was called.

Property of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.localDescription;
```

## <span>Return Value</span>

Returns an object of type RTCSessionDescriptionRTCSessionDescription

Returns a null object if the local description has not yet been set.

**Needs Examples**: This section should include examples.

