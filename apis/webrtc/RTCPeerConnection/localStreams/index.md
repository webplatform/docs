---
title: 'localStreams'
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
  - API_Object_Properties
  - API
  - WebRTC
  - Needs_Examples
uri: apis/webrtc/RTCPeerConnection/localStreams

---
## Summary

Returns an array of MediaStream objects added to the connection with addStream().

Property of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.localStreams;
```

## Return Value

Returns an object of type MediaStreamArrayMediaStreamArray

An array of local [MediaStream](/apis/webrtc/MediaStream) objects that were added with [addStream()](/apis/webrtc/RTCPeerConnection/addStream).

