---
title: vertical
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
summary: 'A string representing the text track cue writing direction, as follows. If it is horizontal: The empty string. If it is vertical growing left: The string &quot;rl&quot;. If it is vertical growing right: The string &quot;lr&quot;.'
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
uri: apis/audio-video/TextTrackCue/vertical

---
## <span>Summary</span>

A string representing the text track cue writing direction, as follows. If it is horizontal: The empty string. If it is vertical growing left: The string &quot;rl&quot;. If it is vertical growing right: The string &quot;lr&quot;.

Property of [apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)[apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)

## <span>Syntax</span>

``` js
var result = TextTrackCue.vertical;
TextTrackCue.vertical = value;
```

## <span>Return Value</span>

Returns an object of type StringString

## <span>Examples</span>

``` js
//. . .
var myTrack = document.getElementById("entrack").track; // get text track from track element
var myCues = myTrack.cues;   // get list of cues
for (var i = 0; i < myCues.length; i++) {
// set each cue's vertical flag to vertical-growing-right
myCues[i].vertical = "lr";
}
//. . .
```

## <span>Usage</span>

     "Horizontal" writing direction means a text line extends horizontally and is positioned vertically, with consecutive lines displayed below each other. "Vertical growing left" means a text line extends vertically and is positioned horizontally, with consecutive lines displayed to the left of each other. "Vertical growing right" means a text line extends vertically and is positioned horizontally, with consecutive lines displayed to the right of each other.

## <span>Related specifications</span>

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
