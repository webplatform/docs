---
title: MediaStreamTrackList
tags:
  0: API
  1: Objects
  3: WebRTC
readiness: 'Not Ready'
standardization_status: 'W3C Working Draft'
notes:
  - "\nDeletion Candidate:   The MediaStreamTrackList API object has been removed from the WebRTC Editor's Draft in Nov 13, 2012. Even if MediaStreamTrackList is still used in the WebRTC Working Draft, it is not defined in the Media Capture and Streams Working Drafts after Nov 15, 2012.\n\n"
summary: 'A MediaStream has two MediaStreamTrackList objects, one for the video tracks and one for the audio tracks.'
uri: apis/webrtc/MediaStreamTrackList

---
# MediaStreamTrackList

## Summary

A MediaStream has two MediaStreamTrackList objects, one for the video tracks and one for the audio tracks.

## Properties

API Name
:   Summary
[length](/apis/webrtc/MediaStreamTrackList/length)
:   The number of tracks in the list.
[onaddtrack](/apis/webrtc/MediaStreamTrackList/onaddtrack)
:   Handles the addtrack event.
[onremovetrack](/apis/webrtc/MediaStreamTrackList/onremovetrack)
:   Handles the removetrack event.

## Methods

API Name
:   Summary
[add](/apis/webrtc/MediaStreamTrackList/add)
:   Adds a MediaStreamTrack to this track list.
[item](/apis/webrtc/MediaStreamTrackList/item)
:   Returns the MediaStreamTrack at the specified index value.
[remove](/apis/webrtc/MediaStreamTrackList/remove)
:   Removes a MediaStreamTrack from this track list.

## Events

API Name
:   Summary
[addtrack](/apis/webrtc/MediaStreamTrackList/addtrack)
:   A MediaStreamTrack has been added to the list.
[removetrack](/apis/webrtc/MediaStreamTrackList/removetrack)
:   A MediaStreamTrack has been removed from the list.

**Needs Examples**: This section should include examples.

