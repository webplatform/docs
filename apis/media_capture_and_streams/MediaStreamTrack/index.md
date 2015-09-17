---
title: 'MediaStreamTrack'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Represents a media source in the user agent.'
tags:
  - API_Objects
  - API
  - Media_Capture_and_Streams
uri: 'apis/media capture and streams/MediaStreamTrack'

---
## Summary

Represents a media source in the user agent.

## Properties

[enabled](/apis/media_capture_and_streams/MediaStreamTrack/enabled)
:   Enables the track if the new value is true, and disable it otherwise.

[id](/apis/media_capture_and_streams/MediaStreamTrack/id)
:   A globally unique identifier string, initialized when the MediaStreamTrack object is created.

[kind](/apis/media_capture_and_streams/MediaStreamTrack/kind)
:   Returns the string "audio" if the object represents an audio track or "video" if object represents a video track.

[label](/apis/media_capture_and_streams/MediaStreamTrack/label)
:   Returns the label of the object’s corresponding track, if any. If the corresponding track has or had no label, it returns the empty string.

[muted](/apis/media_capture_and_streams/MediaStreamTrack/muted)
:   Returns true if the track is muted, and false otherwise.

[onended](/apis/media_capture_and_streams/MediaStreamTrack/onended)
:   Handles the ended event when fired on the MediaStreamTrack object.

[onmute](/apis/media_capture_and_streams/MediaStreamTrack/onmute)
:   Handles the mute event when fired on the MediaStreamTrack object.

[onoverconstrained](/apis/media_capture_and_streams/MediaStreamTrack/onoverconstrained)
:   Handles the overcontrained event when fired on the MediaStreamTrack object.

[onstarted](/apis/media_capture_and_streams/MediaStreamTrack/onstarted)
:   Handles the started event when fired on the MediaStreamTrack object.

[onunmute](/apis/media_capture_and_streams/MediaStreamTrack/onunmute)
:   Handles the unmute event when fired on the MediaStreamTrack object.

[readonly](/apis/media_capture_and_streams/MediaStreamTrack/readonly)
:   Returns true If the track (audio or video) is backed by a read-only source such as a file, or the track source is a local microphone or camera, but is shared so that this track cannot modify any of the source's settings. Returns false otherwise.

[readyState](/apis/media_capture_and_streams/MediaStreamTrack/readyState)
:   Returns the state of the track.

[remote](/apis/media_capture_and_streams/MediaStreamTrack/remote)
:   Returns true if the track is sourced by an RTCPeerConnection. Returns false otherwise.

## Methods

[applyConstraints](/apis/media_capture_and_streams/MediaStreamTrack/applyConstraints)
:   Replaces all existing constraints with the provided constraints, if existing constraints exist. Otherwise, it applies the newly provided constraints to the track.

[capabilities](/apis/media_capture_and_streams/MediaStreamTrack/capabilities)
:   Returns a dictionary with all of the capabilities for the track type.

[clone](/apis/media_capture_and_streams/MediaStreamTrack/clone)
:   Clones the given MediaStreamTrack.

[constraints](/apis/media_capture_and_streams/MediaStreamTrack/constraints)
:   Returns the complete constraints object associated with the track. If no mandatory constraints have been defined, the mandatory field will not be present (it will be undefined). If no optional constraints have been defined, the optional field will not be present (it will be undefined). If neither optional, nor mandatory constraints have been created, the value null is returned.

[states](/apis/media_capture_and_streams/MediaStreamTrack/states)
:   Returns an object containing all the state variables associated with the allowed constraints.

[stop](/apis/media_capture_and_streams/MediaStreamTrack/stop)
:   Permanently stop the generation of data for track's source.

## Events

[mute](/apis/media_capture_and_streams/MediaStreamTrack/mute)
:   This event fires when the MediaStreamTrack object's source is temporarily unable to provide data.

[overconstrained](/apis/media_capture_and_streams/MediaStreamTrack/overconstrained)
:   This event fires asynchronously for each affected track (when multiple tracks share the same source) after the user agent has evaluated the current constraints against a given sourceId and is not able to configure the source within the limitations established by the union of imposed constraints.

[started](/apis/media_capture_and_streams/MediaStreamTrack/started)
:   This event fires when the MediaStreamTrack object has just transitioned from the "new" readyState to another state.

[unmute](/apis/media_capture_and_streams/MediaStreamTrack/unmute)
:   This event fires when the MediaStreamTrack object's source is live again after having been temporarily unable to provide data.

## Related specifications

[Media Capture and Streams](http://www.w3.org/TR/mediacapture-streams/)
:   W3C Working Draft
