---
title: label
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the label of the given track, if known, or the empty string otherwise.'
code_samples:
  - 'http://samples.msdn.microsoft.com/Workshop/samples/media/showtracks.htm'
uri: apis/audio-video/AudioTrack/label

---
# label

## Summary

Returns the label of the given track, if known, or the empty string otherwise.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/audio-video/AudioTrack](/apis/audio-video/AudioTrack)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioTrack.label;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

## Examples

``` {.html}
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

Specification
:   Status
[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

