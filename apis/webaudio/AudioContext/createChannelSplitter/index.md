---
title: createChannelSplitter
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
summary: 'Creates a ChannelSplitterNode representing a channel splitter. An exception will be thrown for invalid parameter values.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/createChannelSplitter

---
## Summary

Creates a ChannelSplitterNode representing a channel splitter. An exception will be thrown for invalid parameter values.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

``` js
var  = AudioContext.createChannelSplitter(numberOfInputs);
```

## Parameters

### numberOfInputs

 Data-type
:   unsigned long

(Optional)

Determines the number of inputs. Values of up to 32 must be supported. If not specified, then 6 will be used.

## Return Value

Returns an object of type

ChannelSplitterNode

## Examples

``` js
var audioCtx = new AudioContext();
var splitter = audioCtx.createChannelSplitter(2);
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
