---
title: align
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A string representing the text track cue alignment, as follows. If it is start alignment: the string "start". If it is middle alignment: the string "middle". If it is end alignment: the string "end". If it is left alignment: the string "left". If it is right alignment: the string "right". Default is "middle".'
uri: apis/audio-video/TextTrackCue/align

---
# align

## Summary

A string representing the text track cue alignment, as follows. If it is start alignment: the string "start". If it is middle alignment: the string "middle". If it is end alignment: the string "end". If it is left alignment: the string "left". If it is right alignment: the string "right". Default is "middle".

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)</span></span>

## Syntax

``` {.js}
var result = TextTrackCue.align;
TextTrackCue.align = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

## Examples

``` {.js}
//. . .
var myTrack = document.getElementById("entrack").track; // get text track from track element
var myCues = myTrack.cues;   // get list of cues
for (var i = 0; i < myCues.length; i++) {
// set all cue alignments
myCues[i].align = "left");
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

