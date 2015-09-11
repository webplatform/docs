---
title: track
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
    value: 'DOM Node'
    href: /apis/audio-video/TextTrackCue
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the TextTrack object to which this text track cue belongs, if any, or null otherwise.'
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
uri: apis/audio-video/TextTrackCue/track

---
## <span>Summary</span>

Returns the TextTrack object to which this text track cue belongs, if any, or null otherwise.

Property of [apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)[apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = TextTrackCue.track;
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

## <span>Examples</span>

``` js
//. . .
var myTrack = document.getElementById("entrack").track; // get text track from track element
var myCues = myTrack.cues;   // get list of cues
// return the first cue's text track object (in this case, identical to myTrack above)
var theTrack = myCues[0].track;
//. . .
```

## <span>Related specifications</span>

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
