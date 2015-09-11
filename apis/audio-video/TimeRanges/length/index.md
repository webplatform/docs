---
title: length
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/API/TimeRanges.length)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/audio-video/TimeRanges
    href: /apis/audio-video/TimeRanges
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /apis/audio-video/TimeRanges
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the number of ranges in the object.'
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: Video
uri: apis/audio-video/TimeRanges/length

---
## <span>Summary</span>

Returns the number of ranges in the object.

Property of [apis/audio-video/TimeRanges](/apis/audio-video/TimeRanges)[apis/audio-video/TimeRanges](/apis/audio-video/TimeRanges)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = TimeRanges.length;
```

## <span>Return Value</span>

Returns an object of type unsigned longunsigned long

## <span>Examples</span>

Given a video element with the ID "myVideo", this example looks at the time ranges to determine if the entire video has been loaded.

``` js
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

## <span>Related specifications</span>

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
