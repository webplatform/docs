---
title: createGain
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Creates a GainNode, used to control the volume of audio.'
uri: apis/webaudio/AudioContext/createGain

---
# createGain

## Summary

Creates a GainNode, used to control the volume of audio.

*Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)*

## Syntax

``` {.js}
var  = AudioContext.createGain();
```

## Return Value

Returns an object of type .

GainNode

## Examples

``` {.js}
var audioCtx = new AudioContext();
var gainNode = audioCtx.createGain();
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

