---
title: localStreams
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example, spec reference'
summary: 'Returns an array of MediaStream objects added to the connection with addStream().'
uri: apis/webrtc/RTCPeerConnection/localStreams

---
# localStreams

## Summary

Returns an array of MediaStream objects added to the connection with addStream().

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.localStreams;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">MediaStreamArray</span></span>

An array of local [MediaStream](/apis/webrtc/MediaStream) objects that were added with [addStream()](/apis/webrtc/RTCPeerConnection/addStream).

**Needs Examples**: This section should include examples.

