---
title: gain
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Represents the amount of gain to apply. Its default value is 1 (no gain change). The nominal minValue is 0, but may be set negative for phase inversion. The nominal maxValue is 1, but higher values are allowed (no exception thrown). This parameter is a-rate.'
uri: apis/webaudio/GainNode/gain

---
# gain

## Summary

Represents the amount of gain to apply. Its default value is 1 (no gain change). The nominal minValue is 0, but may be set negative for phase inversion. The nominal maxValue is 1, but higher values are allowed (no exception thrown). This parameter is a-rate.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/GainNode](/apis/webaudio/GainNode)</span></span>

## Syntax

``` {.js}
var result = GainNode.gain;
GainNode.gain = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var gainNode = audioCtx.createGain();
gainNode.gain.value = 0.5;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

