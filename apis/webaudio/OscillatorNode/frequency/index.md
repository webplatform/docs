---
title: frequency
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The frequency (in Hertz) of the periodic waveform. This parameter is a-rate.'
uri: apis/webaudio/OscillatorNode/frequency

---
# frequency

## Summary

The frequency (in Hertz) of the periodic waveform. This parameter is a-rate.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = OscillatorNode.frequency;
```

## Examples

``` {.js}
var oscillator = audioCtx.createOscillator();
oscillator.frequency.value = 3000; // value in hertz
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

