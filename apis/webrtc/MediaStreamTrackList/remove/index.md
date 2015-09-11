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
## <span>Summary</span>

Removes a MediaStreamTrack from this track list.

Method of [apis/webrtc/MediaStreamTrackList](/apis/webrtc/MediaStreamTrackList)[apis/webrtc/MediaStreamTrackList](/apis/webrtc/MediaStreamTrackList)

## <span>Syntax</span>

``` js
 trackList.remove(track);
```

## <span>Parameters</span>

### <span>track</span>

 Data-type
:   MediaStreamTrack

 MediaStreamTrack **track**, required.

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Notes</span>

Exception INVALID\_STATE\_ERR if the stream is finished (all tracks have ended).