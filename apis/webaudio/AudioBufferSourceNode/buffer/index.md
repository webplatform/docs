---
title: buffer
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioBufferSourceNode
    href: /apis/webaudio/AudioBufferSourceNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Represents the audio asset to be played.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioBufferSourceNode/buffer

---
## Summary

Represents the audio asset to be played.

Property of [apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)

## Syntax

``` js
var result = AudioBufferSourceNode.buffer;
AudioBufferSourceNode.buffer = value;
```

## Examples

``` js
var source = audioCtx.createBufferSource();
// from audioCtx.createBuffer, or audioCtx.decodeAudioData
source.buffer = myBuffer;
```

## Related specifications

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
