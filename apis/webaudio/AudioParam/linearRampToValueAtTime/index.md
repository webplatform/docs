---
title: 'linearRampToValueAtTime'
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
summary: 'Schedules a linear continuous change in parameter value from the previous scheduled parameter value to the given value.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioParam/linearRampToValueAtTime

---
## Summary

Schedules a linear continuous change in parameter value from the previous scheduled parameter value to the given value.

Method of [apis/webaudio/AudioParam](/apis/webaudio/AudioParam)[apis/webaudio/AudioParam](/apis/webaudio/AudioParam)

## Syntax

``` js
var  = AudioParam.linearRampToValueAtTime(value, endTime);
```

## Parameters

### value

 Data-type
:   Number

 The value the parameter will linearly ramp to at the given time.

### endTime

 Data-type
:   Number

 The time in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime).

## Return Value

Returns an object of type

## Examples

``` js
var gainNode = audioCtx.createGain();
gainNode.gain.linearRampToValueAtTime(1.0, audioCtx.currentTime + 2); //'gain' is the AudioParam
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
