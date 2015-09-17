---
title: 'createDynamicsCompressor'
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
summary: 'Creates a DynamicsCompressorNode, used to apply compression to audio.'
tags:
  - API_Object_Methods
  - API
  - WebAudio
uri: apis/webaudio/AudioContext/createDynamicsCompressor

---
## Summary

Creates a DynamicsCompressorNode, used to apply compression to audio.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

``` js
var  = AudioContext.createDynamicsCompressor();
```

## Return Value

Returns an object of type

DynamicsCompressorNode

## Examples

``` js
var audioCtx = new AudioContext();
var compressor = audioCtx.createDynamicsCompressor();
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
