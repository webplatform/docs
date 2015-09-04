---
title: capabilities
tags:
  0: API
  1: Object
  2: Methods
  4: Media
  5: Capture
  6: and
  7: Streams
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example, spec reference'
summary: 'Returns a dictionary with all of the capabilities for the track type.'
uri: 'apis/media capture and streams/MediaStreamTrack/capabilities'

---
# capabilities

## Summary

Returns a dictionary with all of the capabilities for the track type.

*Method of [apis/media\_capture\_and\_streams/MediaStreamTrack](/apis/media_capture_and_streams/MediaStreamTrack)*

## Syntax

``` {.js}
var  = track.capabilities();
```

## Return Value

Returns an object of type .

If the track type is VideoStreamTrack, the AllVideoCapabilities dictionary is returned. If the track type is AudioStreamTrack, the AllAudioCapabilities dictionary is returned.

**Needs Examples**: This section should include examples.

