---
title: track
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/audio-video/TrackEvent
    href: /apis/audio-video/TrackEvent
  return:
    predicate: 'Returns an object of type '
    value: Object
    href: /apis/audio-video/TrackEvent
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the track object (TextTrack, AudioTrack, or VideoTrack) to which the event relates.'
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
uri: apis/audio-video/TrackEvent/track

---
## Summary

Returns the track object (TextTrack, AudioTrack, or VideoTrack) to which the event relates.

Property of [apis/audio-video/TrackEvent](/apis/audio-video/TrackEvent)[apis/audio-video/TrackEvent](/apis/audio-video/TrackEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = object.track;
```

## Return Value

Returns an object of type ObjectObject

## Examples

``` js
//. . .
var myTrack = document.getElementById("entrack").track; // get track from track element
//. . .
```

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)

## Related specifications

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
