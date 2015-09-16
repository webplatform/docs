---
title: 'playbackRate'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioBufferSourceNode
    href: /apis/webaudio/AudioBufferSourceNode
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/webaudio/AudioBufferSourceNode
standardization_status: 'W3C Editor''s Draft'
summary: 'The speed at which to render the audio stream. The default playbackRate value is 1. This parameter is a-rate.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioBufferSourceNode/playbackRate

---
## Summary

The speed at which to render the audio stream. The default playbackRate value is 1. This parameter is a-rate.

Property of [apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)

## Syntax

``` js
var result = AudioBufferSourceNode.playbackRate;
AudioBufferSourceNode.playbackRate = value;
```

## Return Value

Returns an object of type

AudioParam

## Examples

``` js
var source = audioCtx.createBufferSource();
// play 25% faster than normal speed (1.0)
source.playbackRate.value = 1.25;
```

## Related specifications

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
