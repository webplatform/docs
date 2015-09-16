---
title: remove
notes:
  - 'Parent object obsolete; deletion candidate'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webrtc/MediaStreamTrackList
    href: /apis/webrtc/MediaStreamTrackList
standardization_status: 'W3C Working Draft'
summary: 'Removes a MediaStreamTrack from this track list.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebRTC
uri: apis/webrtc/MediaStreamTrackList/remove

---
## Summary

Removes a MediaStreamTrack from this track list.

Method of [apis/webrtc/MediaStreamTrackList](/apis/webrtc/MediaStreamTrackList)[apis/webrtc/MediaStreamTrackList](/apis/webrtc/MediaStreamTrackList)

## Syntax

``` js
 trackList.remove(track);
```

## Parameters

### track

 Data-type
:   MediaStreamTrack

 MediaStreamTrack **track**, required.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

Exception INVALID\_STATE\_ERR if the stream is finished (all tracks have ended).
