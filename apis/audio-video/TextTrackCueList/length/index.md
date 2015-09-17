---
title: 'length'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/audio-video/TextTrackCueList
    href: /apis/audio-video/TextTrackCueList
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /apis/audio-video/TextTrackCueList
standardization_status: 'W3C Editor''s Draft'
summary: 'The length attribute returns the number of cues in the list represented by the TextTrackCueList.'
tags:
  - API_Object_Properties
  - API
  - Audio
  - Video
uri: apis/audio-video/TextTrackCueList/length

---
## Summary

The length attribute returns the number of cues in the list represented by the TextTrackCueList.

Property of [apis/audio-video/TextTrackCueList](/apis/audio-video/TextTrackCueList)[apis/audio-video/TextTrackCueList](/apis/audio-video/TextTrackCueList)

## Syntax

**Note**: This property is read-only.

``` js
var result = TextTrackCueList.length;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Examples

``` js
//. . .
var myTrack = document.getElementById("entrack").track; // get text track from track element
var myCues = myTrack.cues;   // get list of cues
// report how many cues are in the list
alert(myCues.length);
//. . .
```

## Related specifications

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
