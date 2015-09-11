---
title: align
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
summary: 'A string representing the text track cue alignment, as follows. If it is start alignment: the string &quot;start&quot;. If it is middle alignment: the string &quot;middle&quot;. If it is end alignment: the string &quot;end&quot;. If it is left alignment: the string &quot;left&quot;. If it is right alignment: the string &quot;right&quot;. Default is &quot;middle&quot;.'
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
uri: apis/audio-video/TextTrackCue/align

---
## <span>Summary</span>

A string representing the text track cue alignment, as follows. If it is start alignment: the string &quot;start&quot;. If it is middle alignment: the string &quot;middle&quot;. If it is end alignment: the string &quot;end&quot;. If it is left alignment: the string &quot;left&quot;. If it is right alignment: the string &quot;right&quot;. Default is &quot;middle&quot;.

Property of [apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)[apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)

## <span>Syntax</span>

``` js
var result = TextTrackCue.align;
TextTrackCue.align = value;
```

## <span>Return Value</span>

Returns an object of type StringString

## <span>Examples</span>

``` js
//. . .
var myTrack = document.getElementById("entrack").track; // get text track from track element
var myCues = myTrack.cues;   // get list of cues
for (var i = 0; i < myCues.length; i++) {
// set all cue alignments
myCues[i].align = "left");
}
//. . .
```

## <span>Related specifications</span>

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
