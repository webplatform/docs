---
title: length
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The length attribute of a TextTrackList object returns the number of text tracks in the list represented by the TextTrackList.'
uri: apis/audio-video/TextTrackList/length

---
# length

## Summary

The length attribute of a TextTrackList object returns the number of text tracks in the list represented by the TextTrackList.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/audio-video/TextTrackList](/apis/audio-video/TextTrackList)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = TextTrackList.length;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
//. . .
var myTextTrackList = document.getElementById("entrack").textTracks;
// report how many text tracks are in the list
alert(myTextTrackList.length);
//. . .
```

## Notes

The maximum number of audio tracks a video can contain has not been defined in the World Wide Web Consortium (W3C) specification.

## Related specifications

Specification
:   Status
[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

