---
title: track
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the track object (TextTrack, AudioTrack, or VideoTrack) to which the event relates.'
uri: apis/audio-video/TrackEvent/track

---
# track

## Summary

Returns the track object (TextTrack, AudioTrack, or VideoTrack) to which the event relates.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/audio-video/TrackEvent](/apis/audio-video/TrackEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = object.track;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

## Examples

``` {.js}
//. . .
var myTrack = document.getElementById("entrack").track; // get track from track element
//. . .
```

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)

## Related specifications

Specification
:   Status
[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

