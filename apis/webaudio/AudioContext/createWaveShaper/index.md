---
title: createWaveShaper
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
summary: 'Creates a WaveShaperNode, used to apply a distortion effect to audio.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/createWaveShaper

---
## <span>Summary</span>

Creates a WaveShaperNode, used to apply a distortion effect to audio.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## <span>Syntax</span>

``` js
var  = AudioContext.createWaveShaper();
```

## <span>Return Value</span>

Returns an object of type<span></span>

WaveShaperNode

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var distortion = audioCtx.createWaveShaper();
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
