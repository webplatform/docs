---
title: 'readyState'
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webrtc/MediaStreamTrack
    href: /apis/webrtc/MediaStreamTrack
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned short'
    href: /apis/webrtc/MediaStreamTrack
standardization_status: 'W3C Working Draft'
summary: 'The track''s ready state; values.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
uri: apis/webrtc/MediaStreamTrack/readyState

---
## Summary

The track's ready state; values.

Property of [apis/webrtc/MediaStreamTrack](/apis/webrtc/MediaStreamTrack)[apis/webrtc/MediaStreamTrack](/apis/webrtc/MediaStreamTrack)

## Syntax

**Note**: This property is read-only.

``` js
var state = track.readyState;
```

## Return Value

Returns an object of type unsigned shortunsigned short

-   LIVE (0)- the track is active; the output may be switched on and off with the enabled attribute.
-   MUTED (1) - the track's underlying media source is temporarily unable to provide realtime data.
-   ENDED (2) - the track has ended, and the underlying media source will not provide further data.

**Needs Examples**: This section should include examples.

