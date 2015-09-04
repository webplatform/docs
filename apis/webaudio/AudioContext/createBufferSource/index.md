---
title: createBufferSource
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Creates an AudioBufferSourceNode that can be used to play audio data contained within an AudioBuffer object..'
uri: apis/webaudio/AudioContext/createBufferSource

---
# createBufferSource

## Summary

Creates an AudioBufferSourceNode that can be used to play audio data contained within an AudioBuffer object..

*Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)*

## Syntax

``` {.js}
var  = AudioContext.createBufferSource();
```

## Return Value

Returns an object of type .

AudioBufferSourceNode

## Examples

``` {.js}
var audioCtx = new AudioContext();
var source = audioCtx.createBufferSource();
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

