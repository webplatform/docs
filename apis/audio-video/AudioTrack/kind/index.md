---
title: kind
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the category the given track falls into.'
uri: apis/audio-video/AudioTrack/kind

---
# kind

## Summary

Returns the category the given track falls into.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/audio-video/AudioTrack](/apis/audio-video/AudioTrack)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioTrack.kind;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

-   **"alternative"** : A possible alternative to the main track, e.g. a different take of a song (audio), or a different angle (video). *Applies to: Audio, Video*
-   **"captions"**: A version of the main video track with captions burnt in. (For legacy content; new content would use text tracks.) *Applies to: Video*
-   **"descriptions"**: An audio description of a video track. *Applies to: Audio*
-   **"main"**: The primary audio or video track. *Applies to: Audio, Video*
-   **"main-desc"**: The primary audio track, mixed with audio descriptions. *Applies to: Audio*
-   **"sign"**: A sign-language interpretation of an audio track. *Applies to: Video*
-   **"subtitles"**: A version of the main video track with subtitles burnt in. (For legacy content; new content would use text tracks.) *Applies to: Video*
-   **"translation"**: A translated version of the main audio track. *Applies to: Audio*
-   **"commentary"**: Commentary on the primary audio or video track, e.g. a director's commentary. *Applies to: Audio, Video*
-   **""** (empty string): No explicit kind, or the kind given by the track's metadata is not recognised by the user agent. *Applies to: Audio, Video*

## Examples

``` {.html}
<video id="video1" controls autoplay loop>
    <source src="http://ie.microsoft.com/testdrive/ieblog/2011/nov/pp4_blog_demo.mp4" type="video/mp4" >
    <track id="enTrack" src="entrack.vtt" label="English" kind="subtitles" srclang="en" default>
    <track id="esTrack" src="estrack.vtt" label="Spanish" kind="subtitles" srclang="es">
    <track id="deTrack" src="detrack.vtt" label="German" kind="subtitles" srclang="de">
    HTML5 video not supported
</video>
```

## Related specifications

Specification
:   Status
[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

