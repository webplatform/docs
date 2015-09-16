---
title: 'label'
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
summary: 'Returns the text track label, if there is one, or the empty string otherwise (indicating that a custom label probably needs to be generated from the other attributes of the object if the object is exposed to the user).'
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
uri: apis/audio-video/TextTrack/label

---
## Summary

Returns the text track label, if there is one, or the empty string otherwise (indicating that a custom label probably needs to be generated from the other attributes of the object if the object is exposed to the user).

Property of [apis/audio-video/TextTrack](/apis/audio-video/TextTrack)[apis/audio-video/TextTrack](/apis/audio-video/TextTrack)

## Syntax

**Note**: This property is read-only.

``` js
var result = TextTrack.label;
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
        <button id="mybutton">Show label</button>
    </p>
    <div style="display:block; overflow:auto; height:200px; width:650px;" id="display"></div>

    <script>
      document.getElementById("mybutton").addEventListener("click", function () {
        var myTrack = document.getElementById("entrack").track; // get text track from track element
        var myLabel = myTrack.label;   // get label
        document.getElementById("display").innerHTML = myLabel;
     }, false);
    </script>
</body>
</html>
```

## Related specifications

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
