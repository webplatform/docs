---
title: localDescription
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example, spec reference'
summary: 'Returns the RTCSessionDescription most recently passed to the setLocalDescription() method along with any local candidate descriptions generated since the method was called.'
uri: apis/webrtc/RTCPeerConnection/localDescription

---
# localDescription

## Summary

Returns the RTCSessionDescription most recently passed to the setLocalDescription() method along with any local candidate descriptions generated since the method was called.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.localDescription;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">RTCSessionDescription</span></span>

Returns a null object if the local description has not yet been set.

**Needs Examples**: This section should include examples.

