---
title: 'inBandMetadataTrackDispatchType'
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
summary: "Returns the text track in-band metadata track dispatch type string.\nThis is a string extracted from the media resource specifically for in-band metadata tracks, to enable such tracks to be dispatched to different scripts in the document.\n"
tags:
  - API_Object_Properties
  - API
  - Audio
  - Video
uri: apis/audio-video/TextTrack/inBandMetadataTrackDispatchType

---
## Summary

Returns the text track in-band metadata track dispatch type string. This is a string extracted from the media resource specifically for in-band metadata tracks, to enable such tracks to be dispatched to different scripts in the document.

Property of [apis/audio-video/TextTrack](/apis/audio-video/TextTrack)[apis/audio-video/TextTrack](/apis/audio-video/TextTrack)

## Syntax

**Note**: This property is read-only.

``` js
var result = TextTrack.inBandMetadataTrackDispatchType;
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
        <button id="mybutton">Show dispatch type</button>
    </p>
    <div style="display:block; overflow:auto; height:200px; width:650px;" id="display"></div>

    <script>
      document.getElementById("mybutton").addEventListener("click", function () {
        var myTrack = document.getElementById("entrack").track; // get text track from track element
        var myType = myTrack.inBandMetadataTrackDispatchType;   // get dispatch type
        document.getElementById("display").innerHTML = myType;
     }, false);
    </script>
</body>
</html>
```

## Related specifications

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
