---
title: 'createBiquadFilter'
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
summary: 'Creates a BiquadFilterNode representing a second order filter which can be configured as one of several common filter types.'
tags:
  - API_Object_Methods
  - API
  - WebAudio
uri: apis/webaudio/AudioContext/createBiquadFilter

---
## Summary

Creates a BiquadFilterNode representing a second order filter which can be configured as one of several common filter types.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

``` js
var  = AudioContext.createBiquadFilter();
```

## Return Value

Returns an object of type

BiquadFilter

## Examples

``` js
var audioCtx = new AudioContext();
var biquadFilter = audioCtx.createBiquadFilter();
```

## Related specifications

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
