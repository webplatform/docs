---
title: removeCue
tags:
  0: API
  1: Object
  2: Methods
  4: Audio
  5: Video
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Removes the given cue from textTrack''s text track list of cues.'
uri: apis/audio-video/TextTrack/removeCue

---
# removeCue

## Summary

Removes the given cue from textTrack's text track list of cues.

*Method of [apis/audio-video/TextTrack](/apis/audio-video/TextTrack)*

## Syntax

``` {.js}
var  = TextTrack.removeCue(cue);
```

## Parameters

### cue

 Data-typeÂ
:   String

 "cue" is of type TextTrackCue.

## Return Value

Returns an object of type .

## Examples

``` {.html}
<!DOCTYPE html >
<html >
  <head>
    <title>Remove Cue example</title>
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
</head>
<body>

<video id="video1" controls muted autoplay>
    <source src="video.mp4">
    HTML5 Video not supported
</video>

 <script type="text/javascript">
    var video = document.getElementById("video1");
    var beginTime, endTime, message;
    var newTextTrack = video.addTextTrack("captions", "sample");
    newTextTrack.mode = newTextTrack.SHOWING; // set track to display
    // create some cues and add them to the new track
    for(var i=0;i<10;i++){
        beginTime =  i * 5 ;
        endTime = ( (i * 5) +  5);
        message =  "This is number " + i;
        newTextTrack.addCue(new TextTrackCue(beginTime, endTime, message));
    }
    //  Watch for cue change events
    newTextTrack.addEventListener("cuechange", function () {
            // get current cue, and remove it if it's number 2
            var currentCue = newTextTrack.activeCues[0];
            if (currentCue.text == "This is number 2") {
                newTextTrack.removeCue(currentCue)
            }
        },false);

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

