---
title: 'createMediaElementSource'
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
summary: 'Creates a MediaElementAudioSourceNode, given an HTMLMediaElement. As a consequence of calling this method, audio playback from the HTMLMediaElement will be re-routed into the processing graph of the AudioContext.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/createMediaElementSource

---
## Summary

Creates a MediaElementAudioSourceNode, given an HTMLMediaElement. As a consequence of calling this method, audio playback from the HTMLMediaElement will be re-routed into the processing graph of the AudioContext.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

``` js
var  = AudioContext.createMediaElementSource();
```

## Return Value

Returns an object of type

MediaElementAudioSourceNode

## Examples

``` js
var audioCtx = new AudioContext();
var source = audioCtx.createMediaElementSource(myMediaElement);
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
