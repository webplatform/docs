---
title: reduction
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A read-only decibel value for metering purposes, representing the current amount of gain reduction that the compressor is applying to the signal. If fed no signal the value will be 0 (no gain reduction). The nominal range is -20 to 0. This parameter is k-rate.'
uri: apis/webaudio/DynamicsCompressorNode/reduction

---
# reduction

## Summary

A read-only decibel value for metering purposes, representing the current amount of gain reduction that the compressor is applying to the signal. If fed no signal the value will be 0 (no gain reduction). The nominal range is -20 to 0. This parameter is k-rate.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/DynamicsCompressorNode](/apis/webaudio/DynamicsCompressorNode)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = DynamicsCompressorNode.reduction;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var compressor = audioCtx.createDynamicsCompressor();
compressor.reduction.value = -20;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

