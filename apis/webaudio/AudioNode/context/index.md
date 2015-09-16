---
title: 'context'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioNode
    href: /apis/webaudio/AudioNode
standardization_status: 'W3C Editor''s Draft'
summary: 'The AudioContext that owns this AudioNode.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioNode/context

---
## Summary

The AudioContext that owns this AudioNode.

Property of [apis/webaudio/AudioNode](/apis/webaudio/AudioNode)[apis/webaudio/AudioNode](/apis/webaudio/AudioNode)

## Syntax

**Note**: This property is read-only.

``` js
var result = AudioNode.context;
```

## Examples

``` js
var audioCtx = new AudioContext();
var oscillator = audioCtx.createOscillator();
var cont = oscillator.context; // "audioCtx"
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
