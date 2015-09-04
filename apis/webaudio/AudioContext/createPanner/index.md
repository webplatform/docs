---
title: createPanner
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Creates a PannerNode, used to spatialize an incoming audio stream in 3D space..'
uri: apis/webaudio/AudioContext/createPanner

---
# createPanner

## Summary

Creates a PannerNode, used to spatialize an incoming audio stream in 3D space..

*Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)*

## Syntax

``` {.js}
var  = AudioContext.createPanner();
```

## Return Value

Returns an object of type .

PannerNode

## Examples

``` {.js}
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

