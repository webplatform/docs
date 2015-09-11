---
title: createPanner
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
summary: 'Creates a PannerNode, used to spatialize an incoming audio stream in 3D space..'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/createPanner

---
## <span>Summary</span>

Creates a PannerNode, used to spatialize an incoming audio stream in 3D space..

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## <span>Syntax</span>

``` js
var  = AudioContext.createPanner();
```

## <span>Return Value</span>

Returns an object of type<span></span>

PannerNode

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
