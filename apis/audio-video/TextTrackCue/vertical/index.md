---
title: vertical
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A string representing the text track cue writing direction, as follows. If it is horizontal: The empty string. If it is vertical growing left: The string "rl". If it is vertical growing right: The string "lr".'
uri: apis/audio-video/TextTrackCue/vertical

---
# vertical

## Summary

A string representing the text track cue writing direction, as follows. If it is horizontal: The empty string. If it is vertical growing left: The string "rl". If it is vertical growing right: The string "lr".

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)</span></span>

## Syntax

``` {.js}
var result = TextTrackCue.vertical;
TextTrackCue.vertical = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

## Examples

``` {.js}
//. . .
var myTrack = document.getElementById("entrack").track; // get text track from track element
var myCues = myTrack.cues;   // get list of cues
for (var i = 0; i < myCues.length; i++) {
// set each cue's vertical flag to vertical-growing-right
myCues[i].vertical = "lr";
}
//. . .
```

## Usage

     "Horizontal" writing direction means a text line extends horizontally and is positioned vertically, with consecutive lines displayed below each other. "Vertical growing left" means a text line extends vertically and is positioned horizontally, with consecutive lines displayed to the left of each other. "Vertical growing right" means a text line extends vertically and is positioned horizontally, with consecutive lines displayed to the right of each other.

## Related specifications

Specification
:   Status
[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

