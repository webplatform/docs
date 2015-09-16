---
title: 'numberOfChannels'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioBuffer
    href: /apis/webaudio/AudioBuffer
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/webaudio/AudioBuffer
standardization_status: 'W3C Editor''s Draft'
summary: 'The number of discrete audio channels described by the PCM audio data.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioBuffer/numberOfChannels

---
## Summary

The number of discrete audio channels described by the PCM audio data.

Property of [apis/webaudio/AudioBuffer](/apis/webaudio/AudioBuffer)[apis/webaudio/AudioBuffer](/apis/webaudio/AudioBuffer)

## Syntax

**Note**: This property is read-only.

``` js
var result = AudioBuffer.numberOfChannels;
```

## Return Value

Returns an object of type

Integer

## Examples

``` js
var myArrayBuffer = audioCtx.createBuffer(2, frameCount, audioCtx.sampleRate);
var nc = myArrayBuffer.numberOfChannels;
```

## Related specifications

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
