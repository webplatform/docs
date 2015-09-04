---
title: createDynamicsCompressor
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Creates a DynamicsCompressorNode, used to apply compression to audio.'
uri: apis/webaudio/AudioContext/createDynamicsCompressor

---
# createDynamicsCompressor

## Summary

Creates a DynamicsCompressorNode, used to apply compression to audio.

*Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)*

## Syntax

``` {.js}
var  = AudioContext.createDynamicsCompressor();
```

## Return Value

Returns an object of type .

DynamicsCompressorNode

## Examples

``` {.js}
var audioCtx = new AudioContext();
var compressor = audioCtx.createDynamicsCompressor();
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

