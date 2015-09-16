---
title: TrackEvent
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A TrackEvent object exposes (via its track attribute) the track to which an event relates.'
tags:
  0: API
  1: Objects
  3: Audio
  4: Video
uri: apis/audio-video/TrackEvent

---
## Summary

A TrackEvent object exposes (via its track attribute) the track to which an event relates.

## Properties

API Name
:   Summary

[track](/apis/audio-video/TrackEvent/track)
:   Returns the track object (TextTrack, AudioTrack, or VideoTrack) to which the event relates.

## Methods

*No methods.*

## Events

*No events.*

## Notes

The **onaddtrack** event listener must be added to the **video** object before the video source content is loaded.

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)

## Related specifications

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
