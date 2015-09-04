---
title: readyState
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example, spec reference'
summary: 'The track''s ready state; values.'
uri: apis/webrtc/MediaStreamTrack/readyState

---
# readyState

## Summary

The track's ready state; values.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webrtc/MediaStreamTrack](/apis/webrtc/MediaStreamTrack)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var state = track.readyState;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned short</span></span>

-   LIVE (0)- the track is active; the output may be switched on and off with the enabled attribute.
-   MUTED (1) - the track's underlying media source is temporarily unable to provide realtime data.
-   ENDED (2) - the track has ended, and the underlying media source will not provide further data.

**Needs Examples**: This section should include examples.

