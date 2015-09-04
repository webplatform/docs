---
title: pauseOnExit
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the pause-on-exit flag on a TextTrackCue. When the flag is true, playback will pause when it reaches the cue''s endTime.'
uri: apis/audio-video/TextTrackCue/pauseOnExit

---
# pauseOnExit

## Summary

Returns the pause-on-exit flag on a TextTrackCue. When the flag is true, playback will pause when it reaches the cue's endTime.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = TextTrackCue.pauseOnExit;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

## Examples

This example displays the cue (caption), startTime, endTime, pauseOnExit, and id for all cues in a track.

``` {.html}
  <head>
    <script type="text/javascript">
      function getCues() {
        var myTrack = document.getElementById("entrack").track; // get text track from track element
        var myCues = myTrack.cues;   // get list of cues
        var statusFlags = "<table><tr><th>startTime</th><th>endTime</th>";
        statusFlags += "<th>pauseOnExit</th><th>id</th>";
        statusFlags += "<th>cue text</th></tr>";

        for (var i = 0; i < myCues.length; i++) {
          statusFlags += "<tr><td>" + myCues[i].startTime + "</td><td>" + myCues[i].endTime + "</td>";
          statusFlags += "</td><td>" + +myCues[i].pauseOnExit + "</td><td>\"" + myCues[i].id + "\"</td>";
          statusFlags += "</td><td>" + myCues[i].getCueAsHTML().textContent + "</td></tr>";
          }
          statusFlags += "</table>";
          document.getElementById("display").innerHTML = statusFlags;  //append track label
        }
    </script>
  </head>
  <body>
    <video id="video1" controls  >
      <source src="video.mp4">
      <track id="entrack" label="English subtitles" kind="captions" src="entrack.vtt" srclang="en" default>
    </video>
    <p><button onclick="getCues();">Show tracks</button></p>
    <div style="display:block; overflow:auto; height:200px; width:auto"  id="display"></div>
</body>
```

## Related specifications

Specification
:   Status
[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

