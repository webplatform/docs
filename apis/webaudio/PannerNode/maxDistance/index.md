---
title: maxDistance
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The maximum distance between source and listener, after which the volume will not be reduced any further. The default value is 10000.'
uri: apis/webaudio/PannerNode/maxDistance

---
# maxDistance

## Summary

The maximum distance between source and listener, after which the volume will not be reduced any further. The default value is 10000.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)</span></span>

## Syntax

``` {.js}
var result = PannerNode.maxDistance;
PannerNode.maxDistance = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.maxDistance = 10000;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

