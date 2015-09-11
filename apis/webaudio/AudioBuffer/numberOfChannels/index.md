---
title: numberOfChannels
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
## <span>Summary</span>

The number of discrete audio channels described by the PCM audio data.

Property of [apis/webaudio/AudioBuffer](/apis/webaudio/AudioBuffer)[apis/webaudio/AudioBuffer](/apis/webaudio/AudioBuffer)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = AudioBuffer.numberOfChannels;
```

## <span>Return Value</span>

Returns an object of type<span></span>

Integer

## <span>Examples</span>

``` js
var myArrayBuffer = audioCtx.createBuffer(2, frameCount, audioCtx.sampleRate);
var nc = myArrayBuffer.numberOfChannels;
```

## <span>Related specifications</span>

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
