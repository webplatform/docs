---
title: 'setTargetAtTime'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/AudioParam
    href: /apis/webaudio/AudioParam
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/webaudio/AudioParam
standardization_status: 'W3C Editor''s Draft'
summary: 'Start exponentially approaching the target value at the given time with a rate having the given time constant. Among other uses, this is useful for implementing the decay and release portions of an ADSR envelope. Please note that the parameter value does not immediately change to the target value at the given time, but instead gradually changes to the target value.'
tags:
  - API_Object_Methods
  - API
  - WebAudio
uri: apis/webaudio/AudioParam/setTargetAtTime

---
## Summary

Start exponentially approaching the target value at the given time with a rate having the given time constant. Among other uses, this is useful for implementing the decay and release portions of an ADSR envelope. Please note that the parameter value does not immediately change to the target value at the given time, but instead gradually changes to the target value.

Method of [apis/webaudio/AudioParam](/apis/webaudio/AudioParam)[apis/webaudio/AudioParam](/apis/webaudio/AudioParam)

## Syntax

``` js
var  = AudioParam.setTargetAtTime(target, startTime, timeConstant);
```

## Parameters

### target

 Data-type
:   Number

 The value the parameter will start changing to at the given time.

### startTime

 Data-type
:   Number

 The time in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime).

### timeConstant

 Data-type
:   Number

 The time-constant value of first-order filter (exponential) approach to the target value. The larger this value is, the slower the transition will be.

## Return Value

Returns an object of type

## Examples

``` js
var gainNode = audioCtx.createGain();
gainNode.gain.setTargetAtTime(1.0, audioCtx.currentTime + 1, 0.5); //'gain' is the AudioParam
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
