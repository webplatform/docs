---
title: video
tags:
  0: API
  1: Objects
  3: Video
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'HTML Video element allows creator of a HTML document or view of a Web Application to embed a video for display when a user visits the view or opens HTML document in a web browser.'
uri: apis/audio-video/video

---
# video

## Summary

HTML Video element allows creator of a HTML document or view of a Web Application to embed a video for display when a user visits the view or opens HTML document in a web browser.

<span data-meta="subclass_of" data-type="key">Inherits from <span data-type="value">[HTMLMediaElement](/dom/HTMLMediaElement)</span></span>

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Inherited from HTMLMediaElement

### Properties

API Name
:   Summary
[audioTracks](/dom/HTMLMediaElement/audioTracks)
:
[autobuffer](/dom/HTMLMediaElement/autobuffer)
:
[autoplay](/dom/HTMLMediaElement/autoplay)
:
[buffered](/dom/HTMLMediaElement/buffered)
:
[controls](/dom/HTMLMediaElement/controls)
:   Controls attribute used within a Audio element or Video element displays the default media controls defined by the web browser being used to open HTML document or view of a Web Application.
[currentSrc](/dom/HTMLMediaElement/currentSrc)
:
[currentTime](/dom/HTMLMediaElement/currentTime)
:
[defaultPlaybackRate](/dom/HTMLMediaElement/defaultPlaybackRate)
:
[duration](/dom/HTMLMediaElement/duration)
:
[ended](/dom/HTMLMediaElement/ended)
:
[error](/dom/HTMLMediaElement/error)
:
[loop](/dom/HTMLMediaElement/loop)
:
[muted](/dom/HTMLMediaElement/muted)
:
[networkState](/dom/HTMLMediaElement/networkState)
:
[paused](/dom/HTMLMediaElement/paused)
:
[playbackRate](/dom/HTMLMediaElement/playbackRate)
:
[played](/dom/HTMLMediaElement/played)
:
[preload](/dom/HTMLMediaElement/preload)
:
[seekable](/dom/HTMLMediaElement/seekable)
:
[seeking](/dom/HTMLMediaElement/seeking)
:
[src](/dom/HTMLMediaElement/src)
:
[textTracks](/dom/HTMLMediaElement/textTracks)
:
[volume](/dom/HTMLMediaElement/volume)
:

### Methods

API Name
:   Summary
[canPlayType](/dom/HTMLMediaElement/canPlayType)
:
[load](/dom/HTMLMediaElement/load)
:
[pause](/dom/HTMLMediaElement/pause)
:
[play](/dom/HTMLMediaElement/play)
:   Loads and starts playback of a media resource.

### Events

API Name
:   Summary
[canplay](/dom/HTMLMediaElement/canplay)
:   Fires whenever enough data is available to determine whether a media is playable.
[canplaythrough](/dom/HTMLMediaElement/canplaythrough)
:   Fires when enough data is available to determine whether a media is playable at a normal rate without interruptions.
[progress](/dom/HTMLMediaElement/progress)
:   Fires to indicate progress while downloading media data.

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Beginning with Internet Explorer 9, any audio or video content needs the correct mime type set on the server, or the files won't play. Internet Explorer 9 supports MP3 audio, and MP4 audio and video. WebM audio and video files can be supported by installing the WebM components from [The WebM project](http://go.microsoft.com/fwlink/p/?LinkID=218894). The following table shows the required settings for your web server to host these files correctly.

Media file to serve
:   Extension setting
Audio mp3
:   mp3
Audio mp4
:   m4a
Audio WebM
:   webm
Video mp4
:   mp4
Video webm
:   webm

�

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.6

## See also

### Related pages (MSDN)

-   `HTMLVideoElement`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

