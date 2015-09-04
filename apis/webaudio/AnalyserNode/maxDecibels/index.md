---
title: maxDecibels
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The maximum power value in the scaling range for the FFT analysis data for conversion to unsigned byte values.'
uri: apis/webaudio/AnalyserNode/maxDecibels

---
# maxDecibels

## Summary

The maximum power value in the scaling range for the FFT analysis data for conversion to unsigned byte values.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)</span></span>

## Syntax

``` {.js}
var result = AnalyserNode.maxDecibels;
AnalyserNode.maxDecibels = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
analyser.maxDecibels = -10;
```

## Related specifications

Specification
:   Status
[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

