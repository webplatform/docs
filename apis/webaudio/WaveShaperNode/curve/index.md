---
title: curve
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The shaping curve used for the waveshaping effect. The input signal is nominally within the range -1 -> +1. Each input sample within this range will index into the shaping curve with a signal level of zero corresponding to the center value of the curve array. Any sample value less than -1 will correspond to the first value in the curve array. Any sample value less greater than +1 will correspond to the last value in the curve array.'
uri: apis/webaudio/WaveShaperNode/curve

---
# curve

## Summary

The shaping curve used for the waveshaping effect. The input signal is nominally within the range -1 -\> +1. Each input sample within this range will index into the shaping curve with a signal level of zero corresponding to the center value of the curve array. Any sample value less than -1 will correspond to the first value in the curve array. Any sample value less greater than +1 will correspond to the last value in the curve array.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/WaveShaperNode](/apis/webaudio/WaveShaperNode)</span></span>

## Syntax

``` {.js}
var result = WaveShaperNode.curve;
WaveShaperNode.curve = value;
```

## Examples

``` {.js}
var audioCtx = new AudioContext();
var distortion = audioCtx.createWaveShaper();
distortion.curve = myCurveDataArray; // myCurveDataArray is a Float32Array
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

