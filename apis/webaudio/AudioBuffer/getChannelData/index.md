---
title: getChannelData
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/AudioBuffer
    href: /apis/webaudio/AudioBuffer
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/webaudio/AudioBuffer
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the Float32Array representing the PCM audio data for the specific channel.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioBuffer/getChannelData

---
## <span>Summary</span>

Returns the Float32Array representing the PCM audio data for the specific channel.

Method of [apis/webaudio/AudioBuffer](/apis/webaudio/AudioBuffer)[apis/webaudio/AudioBuffer](/apis/webaudio/AudioBuffer)

## <span>Syntax</span>

``` js
var  = AudioBuffer.getChannelData(channel);
```

## <span>Parameters</span>

### <span>channel</span>

 Data-type
:   unsigned long

 The channel parameter is an index representing the particular channel to get data for. An index value of 0 represents the first channel. This index value MUST be less than [**numberOfChannels**](/apis/webaudio/AudioBuffer/numberOfChannels) or an exception will be thrown.

## <span>Return Value</span>

Returns an object of type<span></span>

Float32Array

## <span>Examples</span>

``` js
var myArrayBuffer = audioCtx.createBuffer(2, frameCount, audioCtx.sampleRate);
var nowBuffering = myArrayBuffer.getChannelData(channel);
```

## <span>Related specifications</span>

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
