---
title: 'frequency'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/OscillatorNode
    href: /apis/webaudio/OscillatorNode
standardization_status: 'W3C Editor''s Draft'
summary: 'The frequency (in Hertz) of the periodic waveform. This parameter is a-rate.'
tags:
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/OscillatorNode/frequency

---
## Summary

The frequency (in Hertz) of the periodic waveform. This parameter is a-rate.

Property of [apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)[apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)

## Syntax

**Note**: This property is read-only.

``` js
var result = OscillatorNode.frequency;
```

## Examples

``` js
var oscillator = audioCtx.createOscillator();
oscillator.frequency.value = 3000; // value in hertz
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
