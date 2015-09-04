---
title: detune
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A detuning value (in cents) which will offset the frequency by the given amount. This parameter is a-rate.'
uri: apis/webaudio/OscillatorNode/detune

---
# detune

## Summary

A detuning value (in cents) which will offset the frequency by the given amount. This parameter is a-rate.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = OscillatorNode.detune;
```

## Examples

``` {.js}
var oscillator = audioCtx.createOscillator();
oscillator.detune.value = 100; // value in cents
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

