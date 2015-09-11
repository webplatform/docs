---
title: localStreams
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
    value: MediaStreamArray
    href: /apis/webrtc/RTCPeerConnection
standardization_status: 'W3C Working Draft'
summary: 'Returns an array of MediaStream objects added to the connection with addStream().'
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
uri: apis/webrtc/RTCPeerConnection/localStreams

---
## <span>Summary</span>

Returns an array of MediaStream objects added to the connection with addStream().

Property of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.localStreams;
```

## <span>Return Value</span>

Returns an object of type MediaStreamArrayMediaStreamArray

An array of local [MediaStream](/apis/webrtc/MediaStream) objects that were added with [addStream()](/apis/webrtc/RTCPeerConnection/addStream).

**Needs Examples**: This section should include examples.

