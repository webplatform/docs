---
title: setTargetAtTime
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Start exponentially approaching the target value at the given time with a rate having the given time constant. Among other uses, this is useful for implementing the decay and release portions of an ADSR envelope. Please note that the parameter value does not immediately change to the target value at the given time, but instead gradually changes to the target value.'
uri: apis/webaudio/AudioParam/setTargetAtTime

---
# setTargetAtTime

## Summary

Start exponentially approaching the target value at the given time with a rate having the given time constant. Among other uses, this is useful for implementing the decay and release portions of an ADSR envelope. Please note that the parameter value does not immediately change to the target value at the given time, but instead gradually changes to the target value.

*Method of [apis/webaudio/AudioParam](/apis/webaudio/AudioParam)*

## Syntax

``` {.js}
var  = AudioParam.setTargetAtTime(target, startTime, timeConstant);
```

## Parameters

### target

 Data-typeÂ
:   Number

 The value the parameter will start changing to at the given time.

### startTime

 Data-typeÂ
:   Number

 The time in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime).

### timeConstant

 Data-typeÂ
:   Number

 The time-constant value of first-order filter (exponential) approach to the target value. The larger this value is, the slower the transition will be.

## Return Value

Returns an object of type .

## Examples

``` {.js}
var gainNode = audioCtx.createGain();
gainNode.gain.setTargetAtTime(1.0, audioCtx.currentTime + 1, 0.5); //'gain' is the AudioParam
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

