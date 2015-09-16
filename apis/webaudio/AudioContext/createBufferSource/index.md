---
title: 'createBufferSource'
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
summary: 'Creates an AudioBufferSourceNode that can be used to play audio data contained within an AudioBuffer object..'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/createBufferSource

---
## Summary

Creates an AudioBufferSourceNode that can be used to play audio data contained within an AudioBuffer object..

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

``` js
var  = AudioContext.createBufferSource();
```

## Return Value

Returns an object of type

AudioBufferSourceNode

## Examples

``` js
var audioCtx = new AudioContext();
var source = audioCtx.createBufferSource();
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
