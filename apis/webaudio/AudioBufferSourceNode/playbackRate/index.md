---
title: playbackRate
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
## <span>Summary</span>

The speed at which to render the audio stream. The default playbackRate value is 1. This parameter is a-rate.

Property of [apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)

## <span>Syntax</span>

``` js
var result = AudioBufferSourceNode.playbackRate;
AudioBufferSourceNode.playbackRate = value;
```

## <span>Return Value</span>

Returns an object of type<span></span>

AudioParam

## <span>Examples</span>

``` js
var source = audioCtx.createBufferSource();
// play 25% faster than normal speed (1.0)
source.playbackRate.value = 1.25;
```

## <span>Related specifications</span>

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
