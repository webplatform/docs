---
title: add
tags:
  0: API
  1: Object
  2: Methods
  4: WebRTC
readiness: 'Not Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Parent object obsolete; deletion candidate'
summary: 'Adds a MediaStreamTrack to this track list.'
uri: apis/webrtc/MediaStreamTrackList/add

---
# add

## Summary

Adds a MediaStreamTrack to this track list.

*Method of [apis/webrtc/MediaStreamTrackList](/apis/webrtc/MediaStreamTrackList)*

## Syntax

``` {.js}
 trackList.add(/* see parameter list */);
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

