---
title: createBufferSource
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
summary: 'Creates an AudioBufferSourceNode that can be used to play audio data contained within an AudioBuffer object..'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/createBufferSource

---
## <span>Summary</span>

Creates an AudioBufferSourceNode that can be used to play audio data contained within an AudioBuffer object..

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## <span>Syntax</span>

``` js
var  = AudioContext.createBufferSource();
```

## <span>Return Value</span>

Returns an object of type<span></span>

AudioBufferSourceNode

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var source = audioCtx.createBufferSource();
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
