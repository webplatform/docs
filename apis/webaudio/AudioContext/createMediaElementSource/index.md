---
title: createMediaElementSource
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Creates a MediaElementAudioSourceNode, given an HTMLMediaElement. As a consequence of calling this method, audio playback from the HTMLMediaElement will be re-routed into the processing graph of the AudioContext.'
uri: apis/webaudio/AudioContext/createMediaElementSource

---
# createMediaElementSource

## Summary

Creates a MediaElementAudioSourceNode, given an HTMLMediaElement. As a consequence of calling this method, audio playback from the HTMLMediaElement will be re-routed into the processing graph of the AudioContext.

*Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)*

## Syntax

``` {.js}
var  = AudioContext.createMediaElementSource();
```

## Return Value

Returns an object of type .

MediaElementAudioSourceNode

## Examples

``` {.js}
var audioCtx = new AudioContext();
var source = audioCtx.createMediaElementSource(myMediaElement);
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

