---
title: createChannelMerger
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
summary: 'Creates a ChannelMergerNode representing a channel merger. An exception will be thrown for invalid parameter values.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/createChannelMerger

---
## <span>Summary</span>

Creates a ChannelMergerNode representing a channel merger. An exception will be thrown for invalid parameter values.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## <span>Syntax</span>

``` js
var  = AudioContext.createChannelMerger(numberOfOutputs);
```

## <span>Parameters</span>

### <span>numberOfOutputs</span>

 Data-type
:   Number

 Determines the number of outputs. Values of up to 32 must be supported. If not specified, then 6 will be used.

## <span>Return Value</span>

Returns an object of type<span></span>

ChannelMergerNode

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var merger = audioCtx.createChannelMerger(2);
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
