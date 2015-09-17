---
title: 'MediaStream'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The MediaStream interface is used to represent streams of media data, typically (but not necessarily) of audio and/or video content, e.g. from a local camera. Each MediaStream object can contain zero or more tracks, in particular audio and video tracks. And each track in a MediaStream object has a corresponding MediaStreamTrack object.'
tags:
  - API_Objects
  - API
  - Media_Capture_and_Streams
uri: 'apis/media capture and streams/MediaStream'

---
## Summary

The MediaStream interface is used to represent streams of media data, typically (but not necessarily) of audio and/or video content, e.g. from a local camera. Each MediaStream object can contain zero or more tracks, in particular audio and video tracks. And each track in a MediaStream object has a corresponding MediaStreamTrack object.

## Properties

[ended](/apis/media_capture_and_streams/MediaStream/ended)
:   Is true if the MediaStream has finished, false otherwise.

[id](/apis/media_capture_and_streams/MediaStream/id)
:   A globally unique identifier string, initialized when the MediaStream object is created.

[onaddtrack](/apis/media_capture_and_streams/MediaStream/onaddtrack)
:   Handles the addtrack event when fired on the MediaStream object.

[onended](/apis/media_capture_and_streams/MediaStream/onended)
:   Handles the ended event when fired on the MediaStream object.

[onremovetrack](/apis/media_capture_and_streams/MediaStream/onremovetrack)
:   Handles the removetrack event when fired on the MediaStream object.

## Methods

*No methods.*

## Events

[addtrack](/apis/media_capture_and_streams/MediaStream/addtrack)
:   This event is fired when a track is added to the MediaStream.

[removetrack](/apis/media_capture_and_streams/MediaStream/removetrack)
:   This event is fired when a track is removed from the MediaStream.

[ended](/apis/media_capture_and_streams/ended)
:   This event is fired when a MediaStream is stopped.

## Related specifications

[Media Capture and Streams](http://www.w3.org/TR/mediacapture-streams/)
:   W3C Working Draft
