---
title: 'size'
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
    value: 'unsigned long'
    href: /apis/audio-video/TextTrackCue
standardization_status: 'W3C Editor''s Draft'
summary: 'The text track cue size.'
tags:
  - API_Object_Properties
  - API
  - Audio
  - Video
uri: apis/audio-video/TextTrackCue/size

---
## Summary

The text track cue size.

Property of [apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)[apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)

## Syntax

``` js
var result = TextTrackCue.size;
TextTrackCue.size = value;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Examples

``` js
//. . .
var myTrack = document.getElementById("entrack").track; // get text track from track element
var myCues = myTrack.cues;   // get list of cues
for (var i = 0; i < myCues.length; i++) {
// report each text track cue size
alert("Cue " + i + " size: " + myCues[i].size);
}
//. . .
```

## Related specifications

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
