---
title: 'createWaveShaper'
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
  - API_Object_Methods
  - API
  - WebAudio
uri: apis/webaudio/AudioContext/createWaveShaper

---
## Summary

Creates a WaveShaperNode, used to apply a distortion effect to audio.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

``` js
var  = AudioContext.createWaveShaper();
```

## Return Value

Returns an object of type

WaveShaperNode

## Examples

``` js
var audioCtx = new AudioContext();
var distortion = audioCtx.createWaveShaper();
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
