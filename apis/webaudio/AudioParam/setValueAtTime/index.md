---
title: setValueAtTime
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
summary: 'Schedules a parameter value change at the given time.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioParam/setValueAtTime

---
## <span>Summary</span>

Schedules a parameter value change at the given time.

Method of [apis/webaudio/AudioParam](/apis/webaudio/AudioParam)[apis/webaudio/AudioParam](/apis/webaudio/AudioParam)

## <span>Syntax</span>

``` js
var  = AudioParam.setValueAtTime(value, startTime);
```

## <span>Parameters</span>

### <span>value</span>

 Data-type
:   Number

 The value the parameter will change to at the given time.

### <span>startTime</span>

 Data-type
:   Number

 The time in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime).

## <span>Return Value</span>

Returns an object of type<span></span>

## <span>Examples</span>

``` js
var gainNode = audioCtx.createGain();
gainNode.gain.setValueAtTime(0.25, audioCtx.currentTime + 1); //'gain' is the AudioParam
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
