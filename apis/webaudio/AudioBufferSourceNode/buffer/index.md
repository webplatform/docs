---
title: buffer
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Represents the audio asset to be played.'
uri: apis/webaudio/AudioBufferSourceNode/buffer

---
# buffer

## Summary

Represents the audio asset to be played.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)</span></span>

## Syntax

``` {.js}
var result = AudioBufferSourceNode.buffer;
AudioBufferSourceNode.buffer = value;
```

## Examples

``` {.js}
var source = audioCtx.createBufferSource();
// from audioCtx.createBuffer, or audioCtx.decodeAudioData
source.buffer = myBuffer;
```

## Related specifications

Specification
:   Status
[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

