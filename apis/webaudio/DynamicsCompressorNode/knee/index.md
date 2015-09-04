---
title: knee
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A decibel value representing the range above the threshold where the curve smoothly transitions to the ratio portion. Its default value is 30, with a nominal range of 0 to 40. This parameter is k-rate.'
uri: apis/webaudio/DynamicsCompressorNode/knee

---
# knee

## Summary

A decibel value representing the range above the threshold where the curve smoothly transitions to the ratio portion. Its default value is 30, with a nominal range of 0 to 40. This parameter is k-rate.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/DynamicsCompressorNode](/apis/webaudio/DynamicsCompressorNode)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = DynamicsCompressorNode.knee;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var compressor = audioCtx.createDynamicsCompressor();
compressor.knee.value = 40;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

