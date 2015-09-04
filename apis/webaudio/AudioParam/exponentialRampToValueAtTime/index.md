---
title: exponentialRampToValueAtTime
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Schedules an exponential continuous change in parameter value from the previous scheduled parameter value to the given value. Parameters representing filter frequencies and playback rate are best changed exponentially because of the way humans perceive sound.'
uri: apis/webaudio/AudioParam/exponentialRampToValueAtTime

---
# exponentialRampToValueAtTime

## Summary

Schedules an exponential continuous change in parameter value from the previous scheduled parameter value to the given value. Parameters representing filter frequencies and playback rate are best changed exponentially because of the way humans perceive sound.

*Method of [apis/webaudio/AudioParam](/apis/webaudio/AudioParam)*

## Syntax

``` {.js}
var  = AudioParam.exponentialRampToValueAtTime(value, endTime);
```

## Parameters

### value

 Data-typeÂ
:   Number

 The value the parameter will exponentially ramp to at the given time. An exception will be thrown if this value is less than or equal to 0, or if the value at the time of the previous event is less than or equal to 0.

### endTime

 Data-typeÂ
:   Number

 The time in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime).

## Return Value

Returns an object of type .

## Examples

``` {.js}
var gainNode = audioCtx.createGain();
gainNode.gain.exponentialRampToValueAtTime(1.0, audioCtx.currentTime + 2); //'gain' is the AudioParam
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

