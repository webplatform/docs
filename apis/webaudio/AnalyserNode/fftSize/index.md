---
title: fftSize
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The size of the FFT (Fast Fourier Transform) used for frequency-domain analysis. Must be a power of two in the range 32-2048; defaults to 2048.'
uri: apis/webaudio/AnalyserNode/fftSize

---
# fftSize

## Summary

The size of the FFT (Fast Fourier Transform) used for frequency-domain analysis. Must be a power of two in the range 32-2048; defaults to 2048.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AnalyserNode.fftSize;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
analyser.fftSize = 2048;
```

## Related specifications

Specification
:   Status
[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

