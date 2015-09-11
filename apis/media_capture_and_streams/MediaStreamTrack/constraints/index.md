---
title: constraints
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/media_capture_and_streams/MediaStreamTrack
    href: /apis/media_capture_and_streams/MediaStreamTrack
  return_type:
    predicate: 'Returns an object of type  '
    value: MediaTrackConstraints
    href: /apis/media_capture_and_streams/MediaStreamTrack
standardization_status: 'W3C Working Draft'
summary: 'Returns the complete constraints object associated with the track. If no mandatory constraints have been defined, the mandatory field will not be present (it will be undefined). If no optional constraints have been defined, the optional field will not be present (it will be undefined). If neither optional, nor mandatory constraints have been created, the value null is returned.'
tags:
  0: API
  1: Object
  2: Methods
  4: Media
  5: Capture
  6: and
  7: Streams
uri: 'apis/media capture and streams/MediaStreamTrack/constraints'

---
## <span>Summary</span>

Returns the complete constraints object associated with the track. If no mandatory constraints have been defined, the mandatory field will not be present (it will be undefined). If no optional constraints have been defined, the optional field will not be present (it will be undefined). If neither optional, nor mandatory constraints have been created, the value null is returned.

Method of [apis/media\_capture\_and\_streams/MediaStreamTrack](/apis/media_capture_and_streams/MediaStreamTrack)[apis/media\_capture\_and\_streams/MediaStreamTrack](/apis/media_capture_and_streams/MediaStreamTrack)

## <span>Syntax</span>

``` js
var  = track.constraints();
```

## <span>Return Value</span>

Returns an object of type MediaTrackConstraintsMediaTrackConstraints

**Needs Examples**: This section should include examples.

