---
title: loop
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioBufferSourceNode
    href: /apis/webaudio/AudioBufferSourceNode
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /apis/webaudio/AudioBufferSourceNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Indicates if the audio data should play in a loop. The default value is false.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioBufferSourceNode/loop

---
## <span>Summary</span>

Indicates if the audio data should play in a loop. The default value is false.

Property of [apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)

## <span>Syntax</span>

``` js
var result = AudioBufferSourceNode.loop;
AudioBufferSourceNode.loop = value;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

## <span>Examples</span>

``` js
var source = audioCtx.createBufferSource();
source.loop = true;
```

## <span>Related specifications</span>

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
