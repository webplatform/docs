---
title: createBuffer
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/AudioContext
    href: /apis/webaudio/AudioContext
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/webaudio/AudioContext
standardization_status: 'W3C Editor''s Draft'
summary: 'Creates an AudioBuffer of the given size. The audio data in the buffer will be zero-initialized (silent). An exception will be thrown if the numberOfChannels or sampleRate are out-of-bounds.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/createBuffer

---
## <span>Summary</span>

Creates an AudioBuffer of the given size. The audio data in the buffer will be zero-initialized (silent). An exception will be thrown if the numberOfChannels or sampleRate are out-of-bounds.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## <span>Syntax</span>

``` js
var  = AudioContext.createBuffer(numberOfChannels, length, sampleRate);
```

## <span>Parameters</span>

### <span>numberOfChannels</span>

 Data-type
:   unsigned long

 Determines how many channels the buffer will have. An implementation must support at least 32 channels.

### <span>length</span>

 Data-type
:   unsigned long

 Determines the size of the buffer in sample-frames.

### <span>sampleRate</span>

 Data-type
:   Number

 Describes the sample-rate of the linear PCM audio data in the buffer in sample-frames per second. An implementation must support sample-rates in at least the range 22050 to 96000.

## <span>Return Value</span>

Returns an object of type<span></span>

AudioBuffer

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var buffer = audioCtx.createBuffer(2, 22050, 44100);
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
