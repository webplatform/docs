---
title: 'curve'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/WaveShaperNode
    href: /apis/webaudio/WaveShaperNode
standardization_status: 'W3C Editor''s Draft'
summary: 'The shaping curve used for the waveshaping effect. The input signal is nominally within the range -1 -&gt; +1. Each input sample within this range will index into the shaping curve with a signal level of zero corresponding to the center value of the curve array. Any sample value less than -1 will correspond to the first value in the curve array. Any sample value less greater than +1 will correspond to the last value in the curve array.'
tags:
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/WaveShaperNode/curve

---
## Summary

The shaping curve used for the waveshaping effect. The input signal is nominally within the range -1 -&gt; +1. Each input sample within this range will index into the shaping curve with a signal level of zero corresponding to the center value of the curve array. Any sample value less than -1 will correspond to the first value in the curve array. Any sample value less greater than +1 will correspond to the last value in the curve array.

Property of [apis/webaudio/WaveShaperNode](/apis/webaudio/WaveShaperNode)[apis/webaudio/WaveShaperNode](/apis/webaudio/WaveShaperNode)

## Syntax

``` js
var result = WaveShaperNode.curve;
WaveShaperNode.curve = value;
```

## Examples

``` js
var audioCtx = new AudioContext();
var distortion = audioCtx.createWaveShaper();
distortion.curve = myCurveDataArray; // myCurveDataArray is a Float32Array
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
