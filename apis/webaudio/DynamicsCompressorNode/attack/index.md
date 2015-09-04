---
title: attack
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The amount of time (in seconds) to reduce the gain by 10dB. Its default value is 0.003, with a nominal range of 0 to 1. This parameter is k-rate.'
uri: apis/webaudio/DynamicsCompressorNode/attack

---
# attack

## Summary

The amount of time (in seconds) to reduce the gain by 10dB. Its default value is 0.003, with a nominal range of 0 to 1. This parameter is k-rate.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/DynamicsCompressorNode](/apis/webaudio/DynamicsCompressorNode)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = DynamicsCompressorNode.attack;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var compressor = audioCtx.createDynamicsCompressor();
compressor.attack.value = 0;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

