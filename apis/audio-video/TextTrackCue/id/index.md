---
title: 'id'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/audio-video/TextTrackCue
    href: /apis/audio-video/TextTrackCue
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/audio-video/TextTrackCue
standardization_status: 'W3C Editor''s Draft'
summary: 'Gets or sets a text track cue identifier.'
tags:
  - API_Object_Properties
  - API
  - Audio
  - Video
uri: apis/audio-video/TextTrackCue/id

---
## Summary

Gets or sets a text track cue identifier.

Property of [apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)[apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)

## Syntax

``` js
var result = TextTrackCue.id;
TextTrackCue.id = value;
```

## Return Value

Returns an object of type StringString

## Examples

``` js
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

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
