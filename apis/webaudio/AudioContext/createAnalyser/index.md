---
title: 'createAnalyser'
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
summary: 'Creates an AnalyserNode.'
tags:
  - API_Object_Methods
  - API
  - WebAudio
uri: apis/webaudio/AudioContext/createAnalyser

---
## Summary

Creates an AnalyserNode.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

``` js
var  = AudioContext.createAnalyser();
```

## Return Value

Returns an object of type

AnalyserNode

## Examples

``` js
var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
```

## Related specifications

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
