---
title: HTMLVideoElement
code_samples:
  - 'http://gist.github.com/7281780'
notes:
  - 'overview, compatibility'
readiness: 'In Progress'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: HTMLMediaElement
    href: /dom/HTMLMediaElement
summary: 'The HTML &lt;video&gt; element is used to embed video content in an HTML or XHTML document.'
tags:
  - API
  - Objects
  - HTML
  - Video
uri: dom/HTMLVideoElement

---
## Summary

The HTML &lt;video&gt; element is used to embed video content in an HTML or XHTML document.

Inherits from [HTMLMediaElement](/dom/HTMLMediaElement)[HTMLMediaElement](/dom/HTMLMediaElement)

## Properties

API Name
:   Summary

[initialTime](/dom/HTMLVideoElement/initialTime)
:   Earliest point in seconds where the playback can (should) start playing

[poster](/dom/HTMLVideoElement/poster)
:   Valid URL to an image ressource that will be displayed until the first frame of the video is available or will be displayed if no valid video ressource is available at all.

[videoHeight](/dom/HTMLVideoElement/videoHeight)
:

[videoWidth](/dom/HTMLVideoElement/videoWidth)
:

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

## Examples

A simple example of showing a video

``` html
<p>This is big buck bunny video.</p>
<video width="350" height="240" controls>
<source src="http://mirrorblender.top-ix.org/peach/bigbuckbunny_movies/big_buck_bunny_480p_stereo.ogg" type="video/ogg">
</video>
```

[View live example](http://code.webplatform.org/gist/7281780)

## Usage

     Currently, there are 3 supported video formats for the <video> element: MP4, WebM, and Ogg
