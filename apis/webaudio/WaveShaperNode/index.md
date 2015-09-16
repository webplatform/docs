---
title: 'WaveShaperNode'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'WaveShaperNode is an AudioNode processor implementing non-linear distortion effects. Non-linear waveshaping distortion is commonly used for both subtle non-linear warming, or for more obvious distortion effects.'
tags:
  0: API
  1: Objects
  3: WebAudio
uri: apis/webaudio/WaveShaperNode

---
## Summary

WaveShaperNode is an AudioNode processor implementing non-linear distortion effects. Non-linear waveshaping distortion is commonly used for both subtle non-linear warming, or for more obvious distortion effects.

## Properties

API Name
:   Summary

[curve](/apis/webaudio/WaveShaperNode/curve)
:   The shaping curve used for the waveshaping effect. The input signal is nominally within the range -1 -\> +1. Each input sample within this range will index into the shaping curve with a signal level of zero corresponding to the center value of the curve array. Any sample value less than -1 will correspond to the first value in the curve array. Any sample value less greater than +1 will correspond to the last value in the curve array.

## Methods

*No methods.*

## Events

*No events.*

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
