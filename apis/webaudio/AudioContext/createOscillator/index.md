---
title: createOscillator
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Creates an OscillatorNode, a source representing a periodic waveform. It basically generates a constant tone..'
uri: apis/webaudio/AudioContext/createOscillator

---
# createOscillator

## Summary

Creates an OscillatorNode, a source representing a periodic waveform. It basically generates a constant tone..

*Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)*

## Syntax

``` {.js}
var  = AudioContext.createOscillator();
```

## Return Value

Returns an object of type .

OscillatorNode

## Examples

``` {.js}
var audioCtx = new AudioContext();
var oscillator = audioCtx.createOscillator();
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

