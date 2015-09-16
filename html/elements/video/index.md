---
title: video
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5314736'
notes:
  - "Rewrite main content\nNeeds information on codec support. Add more examples."
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLVideoElement](/dom/HTMLVideoElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The video tag represents an embedded video'
tags:
  - Markup
  - Elements
  - HTML
  - Video
uri: html/elements/video

---
## Summary

The video tag represents an embedded video

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLVideoElement](/dom/HTMLVideoElement)

## HTML Attributes

-   `autoplay` = "autoplay" or "" (empty string) or empty
    Instructs the UA to automatically begin playback of the video as soon as it can do so without stopping.
-   `preload` = "none" or "metadata" or "auto" or "" (empty string) or empty
    Represents a hint to the UA about whether optimistic downloading of the video itself or its metadata is considered worthwhile.
    -   "none": Hints to the UA that the user is not expected to need the video, or that minimizing unnecessary traffic is desirable.
    -   "metadata": Hints to the UA that the user is not expected to need the video, but that fetching its metadata (dimensions, first frame, track list, duration, and so on) is desirable.
    -   "auto": Hints to the UA that optimistically downloading the entire video is considered desirable.
        Specifying the empty string is equivalent to specifying the value "auto".
-   `controls` = "controls" or "" (empty string) or empty
    Instructs the UA to expose a user interface for controlling playback of the video.
-   `loop` = "loop" or "" (empty string) or empty
    Instructs the UA to seek back to the start of the video upon reaching the end.
-   `poster` = URL potentially surrounded by spaces
    The address of an image file for the UA to show while no video data is available.
-   `height` = non-negative integer
    The height of the video, in CSS pixels.
-   `width` = non-negative integer
    The width of the video, in CSS pixels.
-   `muted` = "muted" or "" (empty string) or empty
    Represents the default state of the audio channel of the video, potentially overriding user preferences.
-   `mediagroup` = string
    Instructs the UA to link multiple videos and/or audio streams together.
-   `src` = URL potentially surrounded by spaces
    The URL for the video.

## Native video playback without plugins

Browsers that support HTML5 video will play the media without the need for external plugins

The video formats is made up by a `video stream` + `audio stream.`

The three common formats for HTML5 video are: MP4, WebM and OGG Vorbis.

    .mp4 = H.264 + AAC
    .ogg = Theora + Vorbis
    .webm = VP8 + Vorbis

## Server MIME Types

Addition to declaring multiple encodings, the web server also needs to be instructed on the association between MIME types and co

See [MIME types](/concepts/internet_and_web/mime_types) to find more information about MIME types and [Setting up MIME types on your server](/tutorials/configuring_mimetypes_on_the_server) for more information regarding server setup to deliver HTML5 audio and video content.

## Attributes

The attributes (controls, preload, loop) go inside `<video>` tag to change the behavior of the embedded video.

## What about old browsers?

There are several techniques to ensure that people will be able to access the content we've created. Two of them are covered here: Chrome Frame and Flash Fallback

### Chrome Frame

[[Frame](http://www.google.com/chromeframe?prefersystemlevel=true%7CChrome)] is a plugin for Internet Explorer (up to version 8) that will allow the older browsers to work with HTML5 content (not just video and audio) as if it supported the features natively.

### Flash fallback

You can also use flash as a fallback for when the browser does not support any of the provided formats. Flash supports H264 and Adobe has committed to support the WebM format in their flash player although that time timeline is still not clear. The biggest drawback using Flash as opposed to the Chrome Frame plugin is that you will get the flash player interface instead of whatever UI you built for your video tag. The details of this technique can be seen in the Quick Guide to Implementing the HTML5 Audio tutorial.

``` html
<video width="320" height="240" controls="controls" preload="none">
  <source src="movie.mp4" type="video/mp4"/>
  <source src="movie.ogg" type="video/ogg"/>
  <source src="movie.webm" type="video/webm"/>
  <object data="movie.mp4" width="320" height="240">
    <embed src="movie.swf" width="320" height="240"/>
  </object>
</video>
```

## Accessibility

Authors should ensure that the information and user interface components must be presentable to users in ways they can perceive ([WCAG 2.0 - Principle 1: Perceivable](http://www.w3.org/TR/WCAG20/#perceivable)). This includes providing alternatives for time-based media [Guideline 1.2](http://www.w3.org/TR/WCAG20/#media-equiv).

Work in still in progress proper technical support in HTML5.

## Formats and Codecs

The HTML5 specification does not require a video codec to be supported by all user agents. Thus, one need to provide alternate sources to ensure proper user experience in the existing user agents. Using Ogg/Theora/Vorbis and MP4/H.264/AAC seems to cover most of the cases out there (if not all). However, Ogg/Theora/Vorbis is being replaced in favor of WebM nowadays. See the wikipedia [browser support table](http://en.wikipedia.org/wiki/Open_video#Table).

## Streaming

The HTML5 specification does not specify a particular streaming method. It is expected that HTTP 1.1 progressive streaming is at least supported. Adaptive/live streaming may be supported as a UA extension. For an example, see the [HTTP Live Streaming Overview](http://developer.apple.com/iphone/library/documentation/NetworkingInternet/Conceptual/StreamingMediaGuide/StreamingMediaGuide.pdf) from Apple.

## Digital Rights Management

The HTML5 specification does not specify a particular digital rights management (DRM) method. It is expected that videos with no DRM are at least supported. DRM may be supported as a UA extension.

## Examples

Desired video file should be within src attribute. As a best practice you should also include the controls attribute to show playback and volume controls

``` html

<video src="video.webm" controls="controls"></video>

```

HTML5 Video Tag can support different encodings

``` html

<video>
            <source src="video.mp4" type="video/mp4" />
            <source src="video.webm" type="video/webm" />
            <source src="video.ogg" type="video/ogg" />
            Your browser does not support the <code>video</code> element.
            You can download it <a href="video.webm">here</a>.
</video>

```

[View live example](http://code.webplatform.org/gist/5314736)

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/embedded-content.html#the-video-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/embedded-content-0.html#the-video-element)
:   W3C Recommendation

## See also

### Related articles

#### Video

-   [audio-video](/apis/audio-video)

-   [enabled](/apis/audio-video/AudioTrack/enabled)

-   [language](/apis/audio-video/AudioTrack/language)

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   [object-fit](/css/properties/object-fit)

-   [EMBED](/html/elements/embed)

-   **video**

-   [MSEPrimer](/tutorials/MSEPrimer)

-   [HTML5 Video and Other Recommendations](/tutorials/video_others)

-   [WebRTC Resources](/tutorials/webrtc_resources)

### External resources

-   [[Video Chapter](http://diveintohtml5.info/video.html%7C)] from Dive into HTML5
