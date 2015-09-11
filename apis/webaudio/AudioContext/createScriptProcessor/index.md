---
title: createScriptProcessor
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
summary: 'Creates a ScriptProcessorNode for direct audio processing using JavaScript. An exception will be thrown if bufferSize or numberOfInputChannels or numberOfOutputChannels are outside the valid range.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/createScriptProcessor

---
## <span>Summary</span>

Creates a ScriptProcessorNode for direct audio processing using JavaScript. An exception will be thrown if bufferSize or numberOfInputChannels or numberOfOutputChannels are outside the valid range.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## <span>Syntax</span>

``` js
var  = AudioContext.createScriptProcessor(bufferSize, numberOfInputChannels, numberOfOutputChannels);
```

## <span>Parameters</span>

### <span>bufferSize</span>

 Data-type
:   unsigned long

 Determines the buffer size in units of sample-frames. It must be one of the following values: 256, 512, 1024, 2048, 4096, 8192, 16384. This value controls how frequently the [**onaudioprocess**](/apis/webaudio/ScriptProcessorNode/onaudioprocess) event handler is called and how many sample-frames need to be processed each call. Lower values for [**bufferSize**](/apis/webaudio/ScriptProcessorNode/bufferSize) will result in a lower (better) latency. Higher values will be necessary to avoid audio breakup and glitches. The value chosen must carefully balance between latency and audio quality.

### <span>numberOfInputChannels</span>

 Data-type
:   unsigned long

(Optional)

Defaults to 2; determines the number of channels for this node's input. Values of up to 32 must be supported.

### <span>numberOfOutputChannels</span>

 Data-type
:   unsigned long

(Optional)

Defaults to 2; determines the number of channels for this node's output. Values of up to 32 must be supported.

## <span>Return Value</span>

Returns an object of type<span></span>

ScriptProcessorNode

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
myScriptProcessor = audioCtx.createScriptProcessor(1024, 1, 1);
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
