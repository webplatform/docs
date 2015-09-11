---
title: frequency
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/OscillatorNode
    href: /apis/webaudio/OscillatorNode
standardization_status: 'W3C Editor''s Draft'
summary: 'The frequency (in Hertz) of the periodic waveform. This parameter is a-rate.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/OscillatorNode/frequency

---
## <span>Summary</span>

The frequency (in Hertz) of the periodic waveform. This parameter is a-rate.

Property of [apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)[apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = OscillatorNode.frequency;
```

## <span>Examples</span>

``` js
var oscillator = audioCtx.createOscillator();
oscillator.frequency.value = 3000; // value in hertz
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
