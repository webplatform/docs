---
title: 'buffer'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/ConvolverNode
    href: /apis/webaudio/ConvolverNode
standardization_status: 'W3C Editor''s Draft'
summary: 'A mono, stereo, or 4-channel AudioBuffer containing the (possibly multi-channel) impulse response used by the ConvolverNode. At the time when this attribute is set, the buffer and the state of the normalize attribute will be used to configure the ConvolverNode with this impulse response having the given normalization.'
tags:
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/ConvolverNode/buffer

---
## Summary

A mono, stereo, or 4-channel AudioBuffer containing the (possibly multi-channel) impulse response used by the ConvolverNode. At the time when this attribute is set, the buffer and the state of the normalize attribute will be used to configure the ConvolverNode with this impulse response having the given normalization.

Property of [apis/webaudio/ConvolverNode](/apis/webaudio/ConvolverNode)[apis/webaudio/ConvolverNode](/apis/webaudio/ConvolverNode)

## Syntax

``` js
var result = ConvolverNode.buffer;
ConvolverNode.buffer = value;
```

## Examples

``` js
var audioCtx = new AudioContext();
var convolver = audioCtx.createConvolver();
convolver.buffer = myAudioBuffer;
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
