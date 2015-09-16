---
title: 'label'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://samples.msdn.microsoft.com/Workshop/samples/media/showtracks.htm'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/audio-video/AudioTrack
    href: /apis/audio-video/AudioTrack
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/audio-video/AudioTrack
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the label of the given track, if known, or the empty string otherwise.'
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
uri: apis/audio-video/AudioTrack/label

---
## Summary

Returns the label of the given track, if known, or the empty string otherwise.

Property of [apis/audio-video/AudioTrack](/apis/audio-video/AudioTrack)[apis/audio-video/AudioTrack](/apis/audio-video/AudioTrack)

## Syntax

**Note**: This property is read-only.

``` js
var result = AudioTrack.label;
```

## Return Value

Returns an object of type StringString

## Examples

``` html
<video id="video1" controls  >
    <source src="http://ie.microsoft.com/testdrive/Videos/BehindIE9ModernWebStandards/Video.mp4">
    <track id="entrack" label="English subtitles" kind="captions" src="entrack.vtt" srclang="en" default>
    <track id="sptrack" label="Spanish subtitles" kind="captions" src="estrack.vtt" srclang="es">
    <track id="detrack" label="German subtitles" kind="captions" src="detrack.vtt" srclang="de">
  </video>
  <br />
  <button id="gettracks" >View text tracks</button>
  <div id="display"></div>

  <script>
    document.getElementById("gettracks").addEventListener("click", function () {
      var display = document.getElementById("display");
      display.innerHTML = "";
      var mytracks = document.getElementById("video1").textTracks;  //  get the textTrackList
      for (var i = 0; i < mytracks.length; i++) {
        display.innerHTML += (mytracks[i].label + "<br/>");  //append track label to inner text of <div>
      }
    }, false);
</script>
```

[View live example](http://samples.msdn.microsoft.com/Workshop/samples/media/showtracks.htm)

## Related specifications

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
