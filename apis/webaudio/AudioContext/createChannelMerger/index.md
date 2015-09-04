---
title: createChannelMerger
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Creates a ChannelMergerNode representing a channel merger. An exception will be thrown for invalid parameter values.'
uri: apis/webaudio/AudioContext/createChannelMerger

---
# createChannelMerger

## Summary

Creates a ChannelMergerNode representing a channel merger. An exception will be thrown for invalid parameter values.

*Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)*

## Syntax

``` {.js}
var  = AudioContext.createChannelMerger(numberOfOutputs);
```

## Parameters

### numberOfOutputs

 Data-typeÂ
:   Number

 Determines the number of outputs. Values of up to 32 must be supported. If not specified, then 6 will be used.

## Return Value

Returns an object of type .

ChannelMergerNode

## Examples

``` {.js}
var audioCtx = new AudioContext();
var merger = audioCtx.createChannelMerger(2);
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

