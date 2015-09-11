---
title: detune
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/OscillatorNode
    href: /apis/webaudio/OscillatorNode
standardization_status: 'W3C Editor''s Draft'
summary: 'A detuning value (in cents) which will offset the frequency by the given amount. This parameter is a-rate.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/OscillatorNode/detune

---
## <span>Summary</span>

A detuning value (in cents) which will offset the frequency by the given amount. This parameter is a-rate.

Property of [apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)[apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = OscillatorNode.detune;
```

## <span>Examples</span>

``` js
var oscillator = audioCtx.createOscillator();
oscillator.detune.value = 100; // value in cents
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
