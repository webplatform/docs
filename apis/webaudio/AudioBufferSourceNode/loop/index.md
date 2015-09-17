---
title: 'loop'
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
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/AudioBufferSourceNode/loop

---
## Summary

Indicates if the audio data should play in a loop. The default value is false.

Property of [apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)

## Syntax

``` js
var result = AudioBufferSourceNode.loop;
AudioBufferSourceNode.loop = value;
```

## Return Value

Returns an object of type BooleanBoolean

## Examples

``` js
var source = audioCtx.createBufferSource();
source.loop = true;
```

## Related specifications

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
