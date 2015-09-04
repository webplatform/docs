---
title: start
tags:
  0: API
  1: Object
  2: Methods
  4: Audio
  5: Video
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the time for the start of the range with the given index. Throws an IndexSizeError if the index is out of range.'
uri: apis/audio-video/TimeRanges/start

---
# start

## Summary

Returns the time for the start of the range with the given index. Throws an IndexSizeError if the index is out of range.

*Method of [apis/audio-video/TimeRanges](/apis/audio-video/TimeRanges)*

## Syntax

``` {.js}
var object = TimeRanges.start(index);
```

## Parameters

### index

 Data-typeÂ
:   any

 The zero-based index of the item in the collection.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**. This method can return one of these values.

Return code
:   Description
S\_OK
:   The operation completed successfully.
IndexSizeError
:   The specified index is out of range.

## Examples

Given a video element with the ID "myVideo", this example looks at the time ranges to determine if the entire video has been loaded.

``` {.js}
var v = document.GetElementById("myVideo");

var buf = v.buffered;

var numRanges = buf.length;

if (buf.length == 1) {
  // only one range
  if (buf.start(0) == 0 && buf.end(0) == v.duration) {
    // The one range starts at the beginning and ends at
    // the end of the video, so the whole thing is loaded
    var videoLoaded = true;
  }
}
```

## Related specifications

Specification
:   Status
[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/API/TimeRanges.start)

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

