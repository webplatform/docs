---
title: TimeRanges
tags:
  0: API
  1: Objects
  3: Audio
  4: Video
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A TimeRanges object represents the collection of ranges (time periods) from the media resource that have been buffered or played. Ranges in a TimeRanges collection are sequential and not empty. Adjacent ranges are combined together to create longer ones.'
uri: apis/audio-video/TimeRanges

---
# TimeRanges

## Summary

A TimeRanges object represents the collection of ranges (time periods) from the media resource that have been buffered or played. Ranges in a TimeRanges collection are sequential and not empty. Adjacent ranges are combined together to create longer ones.

## Properties

API Name
:   Summary
[length](/apis/audio-video/TimeRanges/length)
:   Returns the number of ranges in the object.

## Methods

API Name
:   Summary
[end](/apis/audio-video/TimeRanges/end)
:   Returns the time for the end of the range with the given index. Throws an IndexSizeError if the index is out of range.
[start](/apis/audio-video/TimeRanges/start)
:   Returns the time for the start of the range with the given index. Throws an IndexSizeError if the index is out of range.

## Events

*No events.*

## Related specifications

Specification
:   Status
[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

