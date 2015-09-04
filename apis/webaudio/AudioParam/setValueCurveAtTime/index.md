---
title: setValueCurveAtTime
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Sets an array of arbitrary parameter values starting at the given time for the given duration. The number of values will be scaled to fit into the desired duration.'
uri: apis/webaudio/AudioParam/setValueCurveAtTime

---
# setValueCurveAtTime

## Summary

Sets an array of arbitrary parameter values starting at the given time for the given duration. The number of values will be scaled to fit into the desired duration.

*Method of [apis/webaudio/AudioParam](/apis/webaudio/AudioParam)*

## Syntax

``` {.js}
var  = AudioParam.setValueCurveAtTime(values, startTime, duration);
```

## Parameters

### values

 Data-typeÂ
:   String

 A **Float32Array** representing a parameter value curve. These values will apply starting at the given time and lasting for the given duration.

### startTime

 Data-typeÂ
:   Number

 The time in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime).

### duration

 Data-typeÂ
:   Number

 The amount of time in seconds (after the time parameter) where values will be calculated according to the values parameter.

## Return Value

Returns an object of type .

## Examples

``` {.js}
var gainNode = audioCtx.createGain();
gainNode.gain.setValueCurveAtTime(waveArray, audioCtx.currentTime, 2); //'gain' is the AudioParam
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

