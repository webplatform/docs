---
title: setValueAtTime
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Schedules a parameter value change at the given time.'
uri: apis/webaudio/AudioParam/setValueAtTime

---
# setValueAtTime

## Summary

Schedules a parameter value change at the given time.

*Method of [apis/webaudio/AudioParam](/apis/webaudio/AudioParam)*

## Syntax

``` {.js}
var  = AudioParam.setValueAtTime(value, startTime);
```

## Parameters

### value

 Data-typeÂ
:   Number

 The value the parameter will change to at the given time.

### startTime

 Data-typeÂ
:   Number

 The time in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime).

## Return Value

Returns an object of type .

## Examples

``` {.js}
var gainNode = audioCtx.createGain();
gainNode.gain.setValueAtTime(0.25, audioCtx.currentTime + 1); //'gain' is the AudioParam
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

