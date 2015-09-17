---
title: 'detune'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/OscillatorNode
    href: /apis/webaudio/OscillatorNode
standardization_status: 'W3C Editor''s Draft'
summary: 'A detuning value (in cents) which will offset the frequency by the given amount. This parameter is a-rate.'
tags:
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/OscillatorNode/detune

---
## Summary

A detuning value (in cents) which will offset the frequency by the given amount. This parameter is a-rate.

Property of [apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)[apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)

## Syntax

**Note**: This property is read-only.

``` js
var result = OscillatorNode.detune;
```

## Examples

``` js
var oscillator = audioCtx.createOscillator();
oscillator.detune.value = 100; // value in cents
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
