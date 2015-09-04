---
title: onaddstream
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example, spec reference'
summary: 'Handles the addstream event fired when setRemoteDescription() is called.'
uri: apis/webrtc/RTCPeerConnection/onaddstream
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/webrtc/RTCPeerConnection/addstream

---
# onaddstream

## Summary

Handles the addstream event fired when setRemoteDescription() is called.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)</span></span>

## Syntax

``` {.js}
var result = element.onaddstream;
element.onaddstream = value;
```

**Needs Examples**: This section should include examples.

## Notes

This is called any time a MediaStream is added by the remote peer. This will be fired only as a result of [setRemoteDescription()](/apis/webrtc/RTCPeerConnection/setRemoteDescription). The onnaddstream callback happens as early as possible after setRemoteDescription(), it does not wait for a given media stream to be accepted or rejected via SDP negotiation.

