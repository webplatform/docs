---
title: 'mode'
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
    value: String
    href: /apis/audio-video/TextTrack
standardization_status: 'W3C Editor''s Draft'
summary: 'The text track mode, represented by a string from the following list. &quot;disabled&quot;: The text track disabled mode. &quot;hidden&quot;: The text track hidden mode. &quot;showing&quot;: The text track showing mode.'
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
uri: apis/audio-video/TextTrack/mode

---
## Summary

The text track mode, represented by a string from the following list. &quot;disabled&quot;: The text track disabled mode. &quot;hidden&quot;: The text track hidden mode. &quot;showing&quot;: The text track showing mode.

Property of [apis/audio-video/TextTrack](/apis/audio-video/TextTrack)[apis/audio-video/TextTrack](/apis/audio-video/TextTrack)

## Syntax

``` js
var result = TextTrack.mode;
TextTrack.mode = value;
```

## Return Value

Returns an object of type StringString

## Examples

``` html
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

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
