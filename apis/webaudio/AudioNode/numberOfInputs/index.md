---
title: 'numberOfInputs'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioNode
    href: /apis/webaudio/AudioNode
standardization_status: 'W3C Editor''s Draft'
summary: 'The number of inputs feeding into the AudioNode. For source nodes, this value will be 0.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioNode/numberOfInputs

---
## Summary

The number of inputs feeding into the AudioNode. For source nodes, this value will be 0.

Property of [apis/webaudio/AudioNode](/apis/webaudio/AudioNode)[apis/webaudio/AudioNode](/apis/webaudio/AudioNode)

## Syntax

**Note**: This property is read-only.

``` js
var result = AudioNode.numberOfInputs;
```

## Examples

``` js
var oscillator = audioCtx.createOscillator();
var inputs = oscillator.numberOfInputs;
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
