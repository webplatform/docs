---
title: LocalMediaStream
tags:
  0: API
  1: Objects
  3: WebRTC
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs spec reference'
summary: 'The LocalMediaStream object is the MediaStream object returned from the call to getUserMedia(). It has all the properties and events of the MediaStream object and the stop method.'
uri: apis/webrtc/LocalMediaStream

---
# LocalMediaStream

## Summary

The LocalMediaStream object is the MediaStream object returned from the call to getUserMedia(). It has all the properties and events of the MediaStream object and the stop method.

<span data-meta="subclass_of" data-type="key">Inherits from <span data-type="value">[MediaStream](/apis/webrtc/MediaStream)</span></span>

## Properties

*No properties.*

## Methods

API Name
:   Summary
[stop](/apis/webrtc/LocalMediaStream/stop)
:   Permanently halts the generation of data for the tracks' sources and removes the references to the sources.

## Events

*No events.*

## Inherited from MediaStream

### Properties

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

### Methods

*No methods.*

### Events

API Name
:   Summary
[ended](/apis/MediaStream/ended)
:   All tracks of the MediaStream object have ended; the MediaStream is said to be finished.

