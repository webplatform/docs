---
title: linearRampToValueAtTime
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Schedules a linear continuous change in parameter value from the previous scheduled parameter value to the given value.'
uri: apis/webaudio/AudioParam/linearRampToValueAtTime

---
# linearRampToValueAtTime

## Summary

Schedules a linear continuous change in parameter value from the previous scheduled parameter value to the given value.

*Method of [apis/webaudio/AudioParam](/apis/webaudio/AudioParam)*

## Syntax

``` {.js}
var  = AudioParam.linearRampToValueAtTime(value, endTime);
```

## Parameters

### value

 Data-typeÂ
:   Number

 The value the parameter will linearly ramp to at the given time.

### endTime

 Data-typeÂ
:   Number

 The time in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime).

## Return Value

Returns an object of type .

## Examples

``` {.js}
var gainNode = audioCtx.createGain();
gainNode.gain.linearRampToValueAtTime(1.0, audioCtx.currentTime + 2); //'gain' is the AudioParam
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

