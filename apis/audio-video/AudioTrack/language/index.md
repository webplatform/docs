---
title: language
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
summary: 'Returns the language of the given track, if known, or the empty string otherwise.'
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
uri: apis/audio-video/AudioTrack/language

---
## <span>Summary</span>

Returns the language of the given track, if known, or the empty string otherwise.

Property of [apis/audio-video/AudioTrack](/apis/audio-video/AudioTrack)[apis/audio-video/AudioTrack](/apis/audio-video/AudioTrack)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = AudioTrack.language;
```

## <span>Return Value</span>

Returns an object of type StringString

## <span>Examples</span>

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

## <span>Related specifications</span>

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft

## <span>See also</span>

### <span>Related articles</span>

#### <span>Audio</span>

-   [audio-video](/apis/audio-video)

-   [enabled](/apis/audio-video/AudioTrack/enabled)

-   **language**

-   [Web Audio API](/apis/webaudio)

-   [value](/apis/webaudio/AudioParam/value)

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   [bgSound](/html/elements/bgSound)

-   [bgsound](/html/elements/bgSound/ja)

-   [implementing html5 audio](/tutorials/implementing_html5_audio)

-   [WebRTC Resources](/tutorials/webrtc_resources)

#### <span>Video</span>

-   [audio-video](/apis/audio-video)

-   [enabled](/apis/audio-video/AudioTrack/enabled)

-   **language**

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   [object-fit](/css/properties/object-fit)

-   [EMBED](/html/elements/embed)

-   [video](/html/elements/video)

-   [MSEPrimer](/tutorials/MSEPrimer)

-   [HTML5 Video and Other Recommendations](/tutorials/video_others)

-   [WebRTC Resources](/tutorials/webrtc_resources)
