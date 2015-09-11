---
title: cancelScheduledValues
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
## <span>Summary</span>

Cancels all scheduled parameter changes with times greater than or equal to startTime.

Method of [apis/webaudio/AudioParam](/apis/webaudio/AudioParam)[apis/webaudio/AudioParam](/apis/webaudio/AudioParam)

## <span>Syntax</span>

``` js
var  = AudioParam.cancelScheduledValues(startTime);
```

## <span>Parameters</span>

### <span>startTime</span>

 Data-type
:   Number

 The starting time at and after which any previously scheduled parameter changes will be cancelled. It is a time in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime).

## <span>Return Value</span>

Returns an object of type<span></span>

## <span>Examples</span>

``` js
var gainNode = audioCtx.createGain();
gainNode.gain.cancelScheduledValues(audioCtx.currentTime); //'gain' is the AudioParam
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
