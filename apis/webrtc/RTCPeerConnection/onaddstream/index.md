---
title: onaddstream
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webrtc/RTCPeerConnection
    href: /apis/webrtc/RTCPeerConnection
standardization_status: 'W3C Working Draft'
summary: 'Handles the addstream event fired when setRemoteDescription() is called.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/webrtc/RTCPeerConnection/addstream
uri: apis/webrtc/RTCPeerConnection/onaddstream

---
## Summary

Handles the addstream event fired when setRemoteDescription() is called.

Property of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## Syntax

``` js
var result = element.onaddstream;
element.onaddstream = value;
```

**Needs Examples**: This section should include examples.

## Notes

This is called any time a MediaStream is added by the remote peer. This will be fired only as a result of [setRemoteDescription()](/apis/webrtc/RTCPeerConnection/setRemoteDescription). The onnaddstream callback happens as early as possible after setRemoteDescription(), it does not wait for a given media stream to be accepted or rejected via SDP negotiation.
