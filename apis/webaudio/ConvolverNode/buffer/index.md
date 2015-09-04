---
title: buffer
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A mono, stereo, or 4-channel AudioBuffer containing the (possibly multi-channel) impulse response used by the ConvolverNode. At the time when this attribute is set, the buffer and the state of the normalize attribute will be used to configure the ConvolverNode with this impulse response having the given normalization.'
uri: apis/webaudio/ConvolverNode/buffer

---
# buffer

## Summary

A mono, stereo, or 4-channel AudioBuffer containing the (possibly multi-channel) impulse response used by the ConvolverNode. At the time when this attribute is set, the buffer and the state of the normalize attribute will be used to configure the ConvolverNode with this impulse response having the given normalization.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/ConvolverNode](/apis/webaudio/ConvolverNode)</span></span>

## Syntax

``` {.js}
var result = ConvolverNode.buffer;
ConvolverNode.buffer = value;
```

## Examples

``` {.js}
var audioCtx = new AudioContext();
var convolver = audioCtx.createConvolver();
convolver.buffer = myAudioBuffer;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

