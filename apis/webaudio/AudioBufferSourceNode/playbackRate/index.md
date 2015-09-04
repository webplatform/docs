---
title: playbackRate
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The speed at which to render the audio stream. The default playbackRate value is 1. This parameter is a-rate.'
uri: apis/webaudio/AudioBufferSourceNode/playbackRate

---
# playbackRate

## Summary

The speed at which to render the audio stream. The default playbackRate value is 1. This parameter is a-rate.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)</span></span>

## Syntax

``` {.js}
var result = AudioBufferSourceNode.playbackRate;
AudioBufferSourceNode.playbackRate = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

AudioParam

## Examples

``` {.js}
var source = audioCtx.createBufferSource();
// play 25% faster than normal speed (1.0)
source.playbackRate.value = 1.25;
```

## Related specifications

Specification
:   Status
[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

