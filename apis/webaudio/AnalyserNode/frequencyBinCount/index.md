---
title: frequencyBinCount
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Half the fftSize (the size of the FFT used for frequency-domain analysis).'
uri: apis/webaudio/AnalyserNode/frequencyBinCount

---
# frequencyBinCount

## Summary

Half the fftSize (the size of the FFT used for frequency-domain analysis).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)</span></span>

## Syntax

``` {.js}
var result = AnalyserNode.frequencyBinCount;
AnalyserNode.frequencyBinCount = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
var bufferLength = analyser.frequencyBinCount;
```

## Related specifications

Specification
:   Status
[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

