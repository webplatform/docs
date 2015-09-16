---
title: 'createConvolver'
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
summary: 'Creates a ConvolverNode, commonly used to add reverb to audio.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/createConvolver

---
## Summary

Creates a ConvolverNode, commonly used to add reverb to audio.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

``` js
var  = AudioContext.createConvolver();
```

## Return Value

Returns an object of type

ConvolverNode

## Examples

``` js
var audioCtx = new AudioContext();
var convolver = audioCtx.createConvolver();
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
