---
title: createConvolver
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Creates a ConvolverNode, commonly used to add reverb to audio.'
uri: apis/webaudio/AudioContext/createConvolver

---
# createConvolver

## Summary

Creates a ConvolverNode, commonly used to add reverb to audio.

*Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)*

## Syntax

``` {.js}
var  = AudioContext.createConvolver();
```

## Return Value

Returns an object of type .

ConvolverNode

## Examples

``` {.js}
var audioCtx = new AudioContext();
var convolver = audioCtx.createConvolver();
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

