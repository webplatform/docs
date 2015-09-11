---
title: readonly
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
  0: API
  1: Object
  2: Properties
  4: Media
  5: Capture
  6: and
  7: Streams
uri: 'apis/media capture and streams/MediaStreamTrack/readonly'

---
## <span>Summary</span>

Returns true If the track (audio or video) is backed by a read-only source such as a file, or the track source is a local microphone or camera, but is shared so that this track cannot modify any of the source's settings. Returns false otherwise.

Property of [apis/media\_capture\_and\_streams/MediaStreamTrack](/apis/media_capture_and_streams/MediaStreamTrack)[apis/media\_capture\_and\_streams/MediaStreamTrack](/apis/media_capture_and_streams/MediaStreamTrack)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = track.readonly;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

**Needs Examples**: This section should include examples.

