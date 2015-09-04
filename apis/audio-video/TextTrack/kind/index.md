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
summary: 'Returns the text track kind string.'
uri: apis/audio-video/TextTrack/kind

---
# kind

## Summary

Returns the text track kind string.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/audio-video/TextTrack](/apis/audio-video/TextTrack)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = TextTrack.kind;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

## Examples

``` {.html}
<video id="video1" controls autoplay loop>
    <source src="http://ie.microsoft.com/testdrive/ieblog/2011/nov/pp4_blog_demo.mp4" type="video/mp4">
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

