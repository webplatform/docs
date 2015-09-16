---
title: MediaStream
code_samples:
  - 'https://github.com/samdutton/simpl/blob/master/getusermedia/wpd.html'
notes:
  - "\nMerge Candidate:  This page is a candidate for merge with the following pages: [[apis/media_capture_and_streams/MediaStream]] \n\n"
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'The MediaStream interface of the WebRTC API describes a stream of audio or video data. A MediaStream object represents a linear, potentially infinite timeline. It is not preloadable, nor is it seekable.'
tags:
  0: API
  1: Objects
  3: WebRTC
uri: apis/webrtc/MediaStream

---
## Summary

The MediaStream interface of the WebRTC API describes a stream of audio or video data. A MediaStream object represents a linear, potentially infinite timeline. It is not preloadable, nor is it seekable.

## Properties

API Name
:   Summary

[audioTracks](/apis/webrtc/MediaStream/audioTracks)
:   The MediaStreamTrackList object representing the audio tracks.

[ended](/apis/webrtc/MediaStream/ended)
:   True if the ended event has fired on the MediaStream object.

[label](/apis/webrtc/MediaStream/label)
:   A globally unique identifier (GUID) of 36 characters that describes the media stream.

[onended](/apis/webrtc/MediaStream/onended)
:   Handles the ended event when fired on the MediaStream object.

[videoTracks](/apis/webrtc/MediaStream/videoTracks)
:   The MediaStreamTrackList object representing the video tracks.

## Methods

*No methods.*

## Events

API Name
:   Summary

[ended](/apis/MediaStream/ended)
:   All tracks of the MediaStream object have ended; the MediaStream is said to be finished.

## Examples

``` js
navigator.getUserMedia =
    navigator.getUserMedia
```

[View live example](https://github.com/samdutton/simpl/blob/master/getusermedia/wpd.html)

## Related specifications

[WebRTC 1.0: Real-time Communication Between Browsers](http://www.w3.org/TR/webrtc/)
:   Working Draft

[Media Capture and Streams](http://www.w3.org/TR/mediacapture-streams/)
:   Working Draft
