---
title: 'LocalMediaStream'
notes:
  - 'Needs spec reference'
readiness: 'In Progress'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: MediaStream
    href: /apis/webrtc/MediaStream
standardization_status: 'W3C Working Draft'
summary: 'The LocalMediaStream object is the MediaStream object returned from the call to getUserMedia(). It has all the properties and events of the MediaStream object and the stop method.'
tags:
  - API_Objects
  - API
  - WebRTC
uri: apis/webrtc/LocalMediaStream

---
## Summary

The LocalMediaStream object is the MediaStream object returned from the call to getUserMedia(). It has all the properties and events of the MediaStream object and the stop method.

Inherits from [MediaStream](/apis/webrtc/MediaStream)[MediaStream](/apis/webrtc/MediaStream)

## Properties

*No properties.*

## Methods

[stop](/apis/webrtc/LocalMediaStream/stop)
:   Permanently halts the generation of data for the tracks' sources and removes the references to the sources.

## Events

*No events.*

## Inherited from MediaStream

### Properties

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

### Methods

*No methods.*

### Events

[ended](/apis/MediaStream/ended)
:   All tracks of the MediaStream object have ended; the MediaStream is said to be finished.
