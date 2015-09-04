---
title: endTime
tags:
  - API
  - Object
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The text track cue end time, in seconds.'
uri: apis/audio-video/TextTrackCue/endTime

---
# endTime

## Summary

The text track cue end time, in seconds.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)</span></span>

## Syntax

``` {.js}
var result = TextTrackCue.endTime;
TextTrackCue.endTime = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

This example adds start times, end times, and captions to a track.

``` {.html}
<!DOCTYPE html >

<html >
  <head>
    <title>Add Text Tracks example</title>
</head>
<body>

<video id="video1" controls="controls" muted="muted">
     <!-- change to your own mp4 video file -->
  <source src="http://ie.microsoft.com/testdrive/Videos/BehindIE9ModernWebStandards/Video.mp4" />
  HTML5 Video not supported
</video>

 <script>
   var video = document.getElementById("video1");
   var startTime, endTime, message;
   var newTextTrack = video.addTextTrack("captions", "sample");
   newTextTrack.mode = newTextTrack.SHOWING; // set track to display
   // create some cues and add them to the new track
   for (var i = 0; i < 30; i++) {
     startTime = i * 5;
     endTime = ((i * 5) + 5);
     message = "This is number " + i;
     newTextTrack.addCue(new TextTrackCue(startTime, endTime, message));
   }
   video.play();
  </script>
</body>
</html>
```

## Related specifications

Specification
:   Status
[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

