---
title: 'getCueAsHTML'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/audio-video/TextTrackCue
    href: /apis/audio-video/TextTrackCue
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/audio-video/TextTrackCue
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the text track cue text as a DocumentFragment of HTML elements and other DOM nodes.'
tags:
  - API_Object_Methods
  - API
  - Audio
  - Video
uri: apis/audio-video/TextTrackCue/getCueAsHTML

---
## Summary

Returns the text track cue text as a DocumentFragment of HTML elements and other DOM nodes.

Method of [apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)[apis/audio-video/TextTrackCue](/apis/audio-video/TextTrackCue)

## Syntax

``` js
var object = TextTrackCue.getCueAsHTML();
```

## Return Value

Returns an object of type DOM NodeDOM Node

DocumentFragment: A document fragment that represents the [TextTrackCue](/apis/audio-video/TextTrackCue) text.

## Examples

The HTML nodes replace the span element that is the first child of the div.

``` html
<head>
<script type="text/javascript">
    document.addEventListener("DOMContentLoaded", function () {  // don't run this until all DOM content is loaded
      var track = document.getElementById("track1");
      track.addEventListener("cuechange", function () {
        var myTrack = this.track;             // track element is "this"
        var myCues = myTrack.activeCues;      // activeCues is an array of current cues.
        if (myCues.length > 0) {
          var disp = document.getElementById("display");
          disp.replaceChild((myCues[0].getCueAsHTML()), disp.firstChild);
        }
      }, false);
    }, false);
    </script>
  </head>
  <body>
    <video id="video1" controls>
      <source src="video.mp4"  >
      <track id='track1' label='English captions' src="entrack.vtt" kind='subtitles' srclang='en' default >
    </video>
    <div id="display">
      
    </div>
```

## Related specifications

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
