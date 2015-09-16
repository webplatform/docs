---
title: type
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/OscillatorNode
    href: /apis/webaudio/OscillatorNode
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned short'
    href: /apis/webaudio/OscillatorNode
standardization_status: 'W3C Editor''s Draft'
summary: 'The shape of the periodic waveform. It may directly be set to any of the type constant values except for CUSTOM. The setWaveTable() method can be used to set a custom waveform, which results in this attribute being set to CUSTOM.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/OscillatorNode/type

---
## Summary

The shape of the periodic waveform. It may directly be set to any of the type constant values except for CUSTOM. The setWaveTable() method can be used to set a custom waveform, which results in this attribute being set to CUSTOM.

Property of [apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)[apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)

## Syntax

``` js
var result = OscillatorNode.type;
OscillatorNode.type = value;
```

## Return Value

Returns an object of type unsigned shortunsigned short

Uses one of the following constant values:

-   SINE (0);
-   SQUARE (1);
-   SAWTOOTH (2);
-   TRIANGLE (3);
-   CUSTOM (4).

## Examples

``` js
var oscillator = audioCtx.createOscillator();
oscillator.type = 'square';
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
