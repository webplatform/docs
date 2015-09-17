---
title: 'readonly'
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/media_capture_and_streams/MediaStreamTrack
    href: /apis/media_capture_and_streams/MediaStreamTrack
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /apis/media_capture_and_streams/MediaStreamTrack
standardization_status: 'W3C Working Draft'
summary: 'Returns true If the track (audio or video) is backed by a read-only source such as a file, or the track source is a local microphone or camera, but is shared so that this track cannot modify any of the source''s settings. Returns false otherwise.'
tags:
  - API_Object_Properties
  - API
  - Media_Capture_and_Streams
  - Needs_Examples
uri: 'apis/media capture and streams/MediaStreamTrack/readonly'

---
## Summary

Returns true If the track (audio or video) is backed by a read-only source such as a file, or the track source is a local microphone or camera, but is shared so that this track cannot modify any of the source's settings. Returns false otherwise.

Property of [apis/media\_capture\_and\_streams/MediaStreamTrack](/apis/media_capture_and_streams/MediaStreamTrack)[apis/media\_capture\_and\_streams/MediaStreamTrack](/apis/media_capture_and_streams/MediaStreamTrack)

## Syntax

**Note**: This property is read-only.

``` js
var result = track.readonly;
```

## Return Value

Returns an object of type BooleanBoolean

