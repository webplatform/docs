---
title: getChannelData
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the Float32Array representing the PCM audio data for the specific channel.'
uri: apis/webaudio/AudioBuffer/getChannelData

---
# getChannelData

## Summary

Returns the Float32Array representing the PCM audio data for the specific channel.

*Method of [apis/webaudio/AudioBuffer](/apis/webaudio/AudioBuffer)*

## Syntax

``` {.js}
var  = AudioBuffer.getChannelData(channel);
```

## Parameters

### channel

 Data-typeÂ
:   unsigned long

 The channel parameter is an index representing the particular channel to get data for. An index value of 0 represents the first channel. This index value MUST be less than [**numberOfChannels**](/apis/webaudio/AudioBuffer/numberOfChannels) or an exception will be thrown.

## Return Value

Returns an object of type .

Float32Array

## Examples

``` {.js}
var myArrayBuffer = audioCtx.createBuffer(2, frameCount, audioCtx.sampleRate);
var nowBuffering = myArrayBuffer.getChannelData(channel);
```

## Related specifications

Specification
:   Status
[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

