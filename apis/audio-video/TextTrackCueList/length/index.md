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
summary: 'The length attribute returns the number of cues in the list represented by the TextTrackCueList.'
uri: apis/audio-video/TextTrackCueList/length

---
# length

## Summary

The length attribute returns the number of cues in the list represented by the TextTrackCueList.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/audio-video/TextTrackCueList](/apis/audio-video/TextTrackCueList)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = TextTrackCueList.length;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
//. . .
var myTrack = document.getElementById("entrack").track; // get text track from track element
var myCues = myTrack.cues;   // get list of cues
// report how many cues are in the list
alert(myCues.length);
//. . .
```

## Related specifications

Specification
:   Status
[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

