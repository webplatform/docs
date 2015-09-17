---
title: 'track'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Duplicate info of that in apis/audio-video/TextTrack? Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: HTMLMediaElement
    href: /dom/HTMLMediaElement
tags:
  - API_Objects
  - API
  - Audio
  - Video
  - Needs_Summary
  - Needs_Examples
uri: apis/audio-video/track

---
Inherits from [HTMLMediaElement](/dom/HTMLMediaElement)[HTMLMediaElement](/dom/HTMLMediaElement)

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Inherited from HTMLMediaElement

### Properties

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

[canPlayType](/dom/HTMLMediaElement/canPlayType)
:

[load](/dom/HTMLMediaElement/load)
:

[pause](/dom/HTMLMediaElement/pause)
:

[play](/dom/HTMLMediaElement/play)
:   Loads and starts playback of a media resource.

### Events

[canplay](/dom/HTMLMediaElement/canplay)
:   Fires whenever enough data is available to determine whether a media is playable.

[canplaythrough](/dom/HTMLMediaElement/canplaythrough)
:   Fires when enough data is available to determine whether a media is playable at a normal rate without interruptions.

[progress](/dom/HTMLMediaElement/progress)
:   Fires to indicate progress while downloading media data.

## Notes

### Remarks

The **HTMLTrackElement** represents a timed text file to provide users with multiple languages or commentary for videos. You can use multiple tracks, and set one as default to be used when the video starts. The text is displayed in the lower portion of the video player. At this time the position and color can't be controlled, but you can retrieve text through script and display it in your own way. The user can choose alternate tracks, or turn tracks off through a built-in user interface or script. Text tracks use a simplified version of the Web Video Text Track (WebVTT) or Timed Text Markup Language (TTML) timed text file formats.Internet Explorer 10 and Metro style apps using JavaScript currently support only timing cues and text captions.

#### WEBVTT

WebVTT files are 8-bit Unicode Transformation Format (UTF-8) format text files that look like the following.

    WEBVTT

    00:00:01.878 --> 00:00:05.334
    Good day everyone, my name is John Smith

    00:00:08.608 --> 00:00:15.296
    This video will teach you how to
    build a sand castle on any beach

The file starts with the tag "WEBVTT" as the first line, followed by a line feed. The timing cues are in the format "HH:MM:SS.sss". The start and end time cues are separated by a space, two hyphens and a greater-than sign ( --\> ), and another space. The timing cues are on a line by themselves followed by a line feed. Immediately following the cue is the caption text. Text captions can be one or more lines. The only restriction is that there must be no blank lines between lines of text. The MIME type is "text/vtt".

#### TTML

Internet Explorer 10 and Metro style apps using JavaScript use a subset of the TTML file format, which is defined in the TTML specification. Internet Explorer and Metro style apps using JavaScript support the following structure. The TTML file includes XML version, encoding type, namespace declaration, and the language in the root element ("\<tt\>"). This is followed by the" \<body\>" and a "\<div\>" element. Within the "\<div\>" element are the timing cues. The actual times are set as attributes (begin, end) of the opening paragraph tag (\<p\>) and the text is delineated by the closing \</p\> tag. Blank lines and white space are ignored. If there are multiple lines, they are defined by \<br/\> tags. The MIME type for TTML files is **application/ttml+xml**.
