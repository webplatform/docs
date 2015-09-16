---
title: createOscillator
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
summary: 'Creates an OscillatorNode, a source representing a periodic waveform. It basically generates a constant tone..'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/createOscillator

---
## Summary

Creates an OscillatorNode, a source representing a periodic waveform. It basically generates a constant tone..

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

``` js
var  = AudioContext.createOscillator();
```

## Return Value

Returns an object of type

OscillatorNode

## Examples

``` js
var audioCtx = new AudioContext();
var oscillator = audioCtx.createOscillator();
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
