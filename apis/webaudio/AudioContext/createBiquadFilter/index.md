---
title: createBiquadFilter
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
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/createBiquadFilter

---
## <span>Summary</span>

Creates a BiquadFilterNode representing a second order filter which can be configured as one of several common filter types.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## <span>Syntax</span>

``` js
var  = AudioContext.createBiquadFilter();
```

## <span>Return Value</span>

Returns an object of type<span></span>

BiquadFilter

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var biquadFilter = audioCtx.createBiquadFilter();
```

## <span>Related specifications</span>

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
