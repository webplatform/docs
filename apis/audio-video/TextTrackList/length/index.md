---
title: 'length'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/audio-video/TextTrackList
    href: /apis/audio-video/TextTrackList
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /apis/audio-video/TextTrackList
standardization_status: 'W3C Editor''s Draft'
summary: 'The length attribute of a TextTrackList object returns the number of text tracks in the list represented by the TextTrackList.'
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
uri: apis/audio-video/TextTrackList/length

---
## Summary

The length attribute of a TextTrackList object returns the number of text tracks in the list represented by the TextTrackList.

Property of [apis/audio-video/TextTrackList](/apis/audio-video/TextTrackList)[apis/audio-video/TextTrackList](/apis/audio-video/TextTrackList)

## Syntax

**Note**: This property is read-only.

``` js
var result = TextTrackList.length;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Examples

``` js
//. . .
var myTextTrackList = document.getElementById("entrack").textTracks;
// report how many text tracks are in the list
alert(myTextTrackList.length);
//. . .
```

## Notes

The maximum number of audio tracks a video can contain has not been defined in the World Wide Web Consortium (W3C) specification.

## Related specifications

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
