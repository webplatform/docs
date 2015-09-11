---
title: activeCues
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/audio-video/TextTrack
    href: /apis/audio-video/TextTrack
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /apis/audio-video/TextTrack
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the text track cues from the text track list of cues that are currently active (i.e. that start before the current playback position and end after it), as a TextTrackCueList object.'
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
uri: apis/audio-video/TextTrack/activeCues

---
## <span>Summary</span>

Returns the text track cues from the text track list of cues that are currently active (i.e. that start before the current playback position and end after it), as a TextTrackCueList object.

Property of [apis/audio-video/TextTrack](/apis/audio-video/TextTrack)[apis/audio-video/TextTrack](/apis/audio-video/TextTrack)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = TextTrack.activeCues;
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

## <span>Examples</span>

``` html
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>activeCues example</title>

    <script type="text/javascript">
        // don't add this listener until all DOM content is loaded
        document.addEventListener("DOMContentLoaded", function () {
            var track = document.getElementById("track1");
            track.addEventListener("cuechange", function () {
                var myTrack = this.track;
                var myCues = myTrack.activeCues;      // array of current cues.
                //  display the start and end time, and cue text
                if (myCues.length > 0) {
                    var disp = document.getElementById("display");
                    disp.innerHTML = myCues[0].startTime + " --> " + myCues[0].endTime + "  " + myCues[0].getCueAsHTML().textContent;
                }
            }, false);
        }, false);
    </script>
</head>
<body>
    <video id="video1" controls>
        <source src="video.mp4">
        <track id="track1" label="English subtitles" kind="captions" src="entrack.vtt" srclang="en" default>
        HTML5 video is not supported
    </video>
    <div id="display"></div>
</body>
<</html>
```

## <span>Related specifications</span>

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
