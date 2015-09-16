---
title: 'sampleRate'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioBuffer
    href: /apis/webaudio/AudioBuffer
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/webaudio/AudioBuffer
standardization_status: 'W3C Editor''s Draft'
summary: 'The sample rate, in samples per second, for the PCM audio data.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioBuffer/sampleRate

---
## Summary

The sample rate, in samples per second, for the PCM audio data.

Property of [apis/webaudio/AudioBuffer](/apis/webaudio/AudioBuffer)[apis/webaudio/AudioBuffer](/apis/webaudio/AudioBuffer)

## Syntax

**Note**: This property is read-only.

``` js
var result = AudioBuffer.sampleRate;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
var myArrayBuffer = audioCtx.createBuffer(2, frameCount, audioCtx.sampleRate);
var sr = myArrayBuffer.sampleRate;
```

## Related specifications

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
