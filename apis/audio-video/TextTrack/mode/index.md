---
title: mode
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The text track mode, represented by a string from the following list. "disabled": The text track disabled mode. "hidden": The text track hidden mode. "showing": The text track showing mode.'
uri: apis/audio-video/TextTrack/mode

---
# mode

## Summary

The text track mode, represented by a string from the following list. "disabled": The text track disabled mode. "hidden": The text track hidden mode. "showing": The text track showing mode.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/audio-video/TextTrack](/apis/audio-video/TextTrack)</span></span>

## Syntax

``` {.js}
var result = TextTrack.mode;
TextTrack.mode = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

## Examples

``` {.html}
<!DOCTYPE HTML>
<html>
<head>
    <title>Get track example</title>
</head>
<body>
    <h1>Get track example</h1>
    <video id="video1" controls>
        <source src="http://ie.microsoft.com/testdrive/Videos/BehindIE9ModernWebStandards/Video.mp4">
        <track id="entrack" label="English subtitles" kind="captions" src="entrack.vtt" srclang="en" default>
    </video>
    <p>
        <button id="mybutton">Show mode</button>
    </p>
    <div style="display:block; overflow:auto; height:200px; width:650px;" id="display"></div>

    <script>
      document.getElementById("mybutton").addEventListener("click", function () {
        var myTrack = document.getElementById("entrack").track; // get text track from track element
        var myMode = myTrack.mode;   // get mode
        document.getElementById("display").innerHTML = myMode;
     }, false);
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

