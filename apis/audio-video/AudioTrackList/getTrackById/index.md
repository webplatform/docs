---
title: 'getTrackById'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://code.webplatform.org/gist/459f1a0ea9f70009b6fe'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/audio-video/AudioTrackList
    href: /apis/audio-video/AudioTrackList
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/audio-video/AudioTrackList
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the AudioTrack object with the given identifier, or null if no track has that identifier.'
tags:
  - API_Object_Methods
  - API
  - Audio
  - Video
uri: apis/audio-video/AudioTrackList/getTrackById

---
## Summary

Returns the AudioTrack object with the given identifier, or null if no track has that identifier.

Method of [apis/audio-video/AudioTrackList](/apis/audio-video/AudioTrackList)[apis/audio-video/AudioTrackList](/apis/audio-video/AudioTrackList)

## Syntax

``` js
var object = AudioTrackList.getTrackById(id);
```

## Parameters

### id

 Data-type
:   any

## Return Value

Returns an object of type DOM NodeDOM Node

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
