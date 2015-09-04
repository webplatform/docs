---
title: createWaveShaper
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Creates a WaveShaperNode, used to apply a distortion effect to audio.'
uri: apis/webaudio/AudioContext/createWaveShaper

---
# createWaveShaper

## Summary

Creates a WaveShaperNode, used to apply a distortion effect to audio.

*Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)*

## Syntax

``` {.js}
var  = AudioContext.createWaveShaper();
```

## Return Value

Returns an object of type .

WaveShaperNode

## Examples

``` {.js}
var audioCtx = new AudioContext();
var distortion = audioCtx.createWaveShaper();
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

