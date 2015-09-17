---
title: 'loopStart'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioBufferSourceNode
    href: /apis/webaudio/AudioBufferSourceNode
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/webaudio/AudioBufferSourceNode
standardization_status: 'W3C Editor''s Draft'
summary: 'An optional value in seconds where looping should begin if the loop attribute is true. Its default value is 0, and it may usefully be set to any value between 0 and the duration of the buffer.'
tags:
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/AudioBufferSourceNode/loopStart

---
## Summary

An optional value in seconds where looping should begin if the loop attribute is true. Its default value is 0, and it may usefully be set to any value between 0 and the duration of the buffer.

Property of [apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)

## Syntax

``` js
var result = AudioBufferSourceNode.loopStart;
AudioBufferSourceNode.loopStart = value;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
var source = audioCtx.createBufferSource();
source.loopStart = 2;
```

## Related specifications

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
