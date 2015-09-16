---
title: 'id'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/459f1a0ea9f70009b6fe'
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
summary: 'Returns the ID of the given track. This is the ID that can be used with a fragment identifier if the format supports the Media Fragments URI syntax, and that can be used with the getTrackById() method.'
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
uri: apis/audio-video/AudioTrack/id

---
## Summary

Returns the ID of the given track. This is the ID that can be used with a fragment identifier if the format supports the Media Fragments URI syntax, and that can be used with the getTrackById() method.

Property of [apis/audio-video/AudioTrack](/apis/audio-video/AudioTrack)[apis/audio-video/AudioTrack](/apis/audio-video/AudioTrack)

## Syntax

**Note**: This property is read-only.

``` js
var result = AudioTrack.id;
```

## Return Value

Returns an object of type StringString

## Examples

``` js
(function () {
    // grab the video element
    var video = document.getElementById("video");

    video.addEventListener("loadeddata", function () {

        // get the audiotracks from the video when it's loaded
        var audioTracks = video.audioTracks;

        var tracksSelection = document.getElementById("tracksSelection");

        // loop through the audio tracks
        for (var i = 0; i < audioTracks.length; i++) {

            // create options for the dropdownlist with the id's
            // and languages of the tracks
            var opt = document.createElement('option');
            opt.value = audioTracks[i].id;
            opt.text = audioTracks[i].language;

            tracksSelection.add(opt);
        }
    });

    tracksSelection.addEventListener("change", function (e) {
        // when the item of the dropdownlist changes
        // grab the id from the selected option
        var audioTracks = video.audioTracks;
        var track = audioTracks.getTrackById(e.currentTarget.value);

        //disable all tracks to prevent them from playing all at once
        for (var i = 0; i < audioTracks.length; i++) {
            audioTracks.enabled = false;
        }

        //set the selected track for the video
        track.enabled = true;
    });
})();
```

[View live example](http://code.webplatform.org/gist/459f1a0ea9f70009b6fe)

## Related specifications

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
