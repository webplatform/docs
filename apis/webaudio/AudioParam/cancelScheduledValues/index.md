---
title: 'cancelScheduledValues'
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
summary: 'Cancels all scheduled parameter changes with times greater than or equal to startTime.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioParam/cancelScheduledValues

---
## Summary

Cancels all scheduled parameter changes with times greater than or equal to startTime.

Method of [apis/webaudio/AudioParam](/apis/webaudio/AudioParam)[apis/webaudio/AudioParam](/apis/webaudio/AudioParam)

## Syntax

``` js
var  = AudioParam.cancelScheduledValues(startTime);
```

## Parameters

### startTime

 Data-type
:   Number

 The starting time at and after which any previously scheduled parameter changes will be cancelled. It is a time in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime).

## Return Value

Returns an object of type

## Examples

``` js
var gainNode = audioCtx.createGain();
gainNode.gain.cancelScheduledValues(audioCtx.currentTime); //'gain' is the AudioParam
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
