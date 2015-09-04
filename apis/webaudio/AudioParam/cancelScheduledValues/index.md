---
title: cancelScheduledValues
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Cancels all scheduled parameter changes with times greater than or equal to startTime.'
uri: apis/webaudio/AudioParam/cancelScheduledValues

---
# cancelScheduledValues

## Summary

Cancels all scheduled parameter changes with times greater than or equal to startTime.

*Method of [apis/webaudio/AudioParam](/apis/webaudio/AudioParam)*

## Syntax

``` {.js}
var  = AudioParam.cancelScheduledValues(startTime);
```

## Parameters

### startTime

 Data-typeÂ
:   Number

 The starting time at and after which any previously scheduled parameter changes will be cancelled. It is a time in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime).

## Return Value

Returns an object of type .

## Examples

``` {.js}
var gainNode = audioCtx.createGain();
gainNode.gain.cancelScheduledValues(audioCtx.currentTime); //'gain' is the AudioParam
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

