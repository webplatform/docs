---
title: id
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Gets or sets a text track cue identifier.'
uri: apis/audio-video/TextTrackCue/id

---
# id

## Summary

Gets or sets a text track cue identifier.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)</span></span>

## Syntax

``` {.js}
var result = TextTrackCue.id;
TextTrackCue.id = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

## Examples

``` {.js}
//. . .
var myTrack = document.getElementById("entrack").track; // get text track from track element
var myCues = myTrack.cues;   // get list of cues
for (var i = 0; i < myCues.length; i++) {
// set all cue IDs
myCues[i].id = "CID" + i; //CID0, CID1, etc.
}
//. . .
```

## Related specifications

Specification
:   Status
[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

