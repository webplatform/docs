---
title: type
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The shape of the periodic waveform. It may directly be set to any of the type constant values except for CUSTOM. The setWaveTable() method can be used to set a custom waveform, which results in this attribute being set to CUSTOM.'
uri: apis/webaudio/OscillatorNode/type

---
# type

## Summary

The shape of the periodic waveform. It may directly be set to any of the type constant values except for CUSTOM. The setWaveTable() method can be used to set a custom waveform, which results in this attribute being set to CUSTOM.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)</span></span>

## Syntax

``` {.js}
var result = OscillatorNode.type;
OscillatorNode.type = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned short</span></span>

Uses one of the following constant values:

-   SINE (0);
-   SQUARE (1);
-   SAWTOOTH (2);
-   TRIANGLE (3);
-   CUSTOM (4).

## Examples

``` {.js}
var oscillator = audioCtx.createOscillator();
oscillator.type = 'square';
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

