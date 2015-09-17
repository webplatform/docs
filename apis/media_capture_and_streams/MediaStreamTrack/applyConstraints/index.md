---
title: 'applyConstraints'
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/media_capture_and_streams/MediaStreamTrack
    href: /apis/media_capture_and_streams/MediaStreamTrack
standardization_status: 'W3C Working Draft'
summary: 'Replaces all existing constraints with the provided constraints, if existing constraints exist. Otherwise, it applies the newly provided constraints to the track.'
tags:
  - API_Object_Methods
  - API
  - Media_Capture_and_Streams
  - Needs_Examples
uri: 'apis/media capture and streams/MediaStreamTrack/applyConstraints'

---
## Summary

Replaces all existing constraints with the provided constraints, if existing constraints exist. Otherwise, it applies the newly provided constraints to the track.

Method of [apis/media\_capture\_and\_streams/MediaStreamTrack](/apis/media_capture_and_streams/MediaStreamTrack)[apis/media\_capture\_and\_streams/MediaStreamTrack](/apis/media_capture_and_streams/MediaStreamTrack)

## Syntax

``` js
 track.applyConstraints(constraints);
```

## Parameters

### constraints

 Data-type
:   MediaTrackConstraints

(Optional)

A new constraint structure to apply to this track.

## Return Value

No return value
