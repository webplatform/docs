---
title: 'createDelay'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/AudioContext
    href: /apis/webaudio/AudioContext
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/webaudio/AudioContext
standardization_status: 'W3C Editor''s Draft'
summary: 'Creates a DelayNode representing a variable delay line. Default delay is 0 seconds.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/createDelay

---
## Summary

Creates a DelayNode representing a variable delay line. Default delay is 0 seconds.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

``` js
var  = AudioContext.createDelay(maxDelayTime);
```

## Parameters

### maxDelayTime

 Data-type
:   Number

(Optional)

Specifies the maximum delay time in seconds allowed for the delay line. If specified, this value must be greater than zero and less than three minutes or a NOT\_SUPPORTED\_ERR exception will be thrown.

## Return Value

Returns an object of type

DelayNode

## Examples

``` js
var audioCtx = new AudioContext();
var synthDelay = audioCtx.createDelay(5.0);
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
