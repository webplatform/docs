---
title: MediaStreamTrack
notes:
  - "\nMerge Candidate:  This page is a candidate for merge with the following pages: [[apis/media_capture_and_streams/MediaStreamTrack]] \n\n"
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'A MediaStreamTrack is one of two kinds, audio or video, and represents the media source, such as a camera.'
tags:
  0: API
  1: Objects
  3: WebRTC
uri: apis/webrtc/MediaStreamTrack

---
## <span>Summary</span>

A MediaStreamTrack is one of two kinds, audio or video, and represents the media source, such as a camera.

## <span>Properties</span>

API Name
:   Summary

[enabled](/apis/webrtc/MediaStreamTrack/enabled)
:   True if the track is still associated with its source.

[kind](/apis/webrtc/MediaStreamTrack/kind)
:   The value, either **audio** or **video** for the source of the track.

[label](/apis/webrtc/MediaStreamTrack/label)
:   A user agent-assigned string that identifies the track source, as in "internal microphone."

[onended](/apis/webrtc/MediaStreamTrack/onended)
:   Handles the ended event when fired on the MediaStream object.

[onmute](/apis/webrtc/MediaStreamTrack/onmute)
:   Handles the muted event when fired on the MediaStream object.

[readyState](/apis/webrtc/MediaStreamTrack/readyState)
:   The track's ready state; values.

## <span>Methods</span>

*No methods.*

## <span>Events</span>

API Name
:   Summary

[ended](/apis/webrtc/MediaStreamTrack/ended)
:   The MediaStreamTrack object's source will not provide data; this may be caused by the following:
    -   the user has revoked permissions on the application
    -   the source device has been disconnected
    -   the remote peer has stopped sending data
    -   the stop() method was invoked

[muted](/apis/webrtc/MediaStreamTrack/muted)
:   The MediaStreamTrack object's source is temporarily unable to provide data.

[unmuted](/apis/webrtc/MediaStreamTrack/unmuted)
:   The MediaStreamTrack object's source has resumed providing data.

**Needs Examples**: This section should include examples.

