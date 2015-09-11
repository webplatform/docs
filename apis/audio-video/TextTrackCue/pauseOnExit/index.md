---
title: pauseOnExit
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
    value: Boolean
    href: /apis/audio-video/TextTrackCue
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the pause-on-exit flag on a TextTrackCue. When the flag is true, playback will pause when it reaches the cue''s endTime.'
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
uri: apis/audio-video/TextTrackCue/pauseOnExit

---
## <span>Summary</span>

Returns the pause-on-exit flag on a TextTrackCue. When the flag is true, playback will pause when it reaches the cue's endTime.

Property of [apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)[apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = TextTrackCue.pauseOnExit;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

## <span>Examples</span>

This example displays the cue (caption), startTime, endTime, pauseOnExit, and id for all cues in a track.

``` html
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

## <span>Related specifications</span>

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
