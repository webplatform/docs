---
title: remove
tags:
  0: API
  1: Object
  2: Methods
  4: WebRTC
readiness: 'Not Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Parent object obsolete; deletion candidate'
summary: 'Removes a MediaStreamTrack from this track list.'
uri: apis/webrtc/MediaStreamTrackList/remove

---
# remove

## Summary

Removes a MediaStreamTrack from this track list.

*Method of [apis/webrtc/MediaStreamTrackList](/apis/webrtc/MediaStreamTrackList)*

## Syntax

``` {.js}
 trackList.remove(track);
```

## Parameters

### track

 Data-typeÂ
:   MediaStreamTrack

 MediaStreamTrack **track**, required.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

Exception INVALID\_STATE\_ERR if the stream is finished (all tracks have ended).

