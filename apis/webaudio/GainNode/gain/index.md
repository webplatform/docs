---
title: gain
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/GainNode
    href: /apis/webaudio/GainNode
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/webaudio/GainNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Represents the amount of gain to apply. Its default value is 1 (no gain change). The nominal minValue is 0, but may be set negative for phase inversion. The nominal maxValue is 1, but higher values are allowed (no exception thrown). This parameter is a-rate.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/GainNode/gain

---
## Summary

Represents the amount of gain to apply. Its default value is 1 (no gain change). The nominal minValue is 0, but may be set negative for phase inversion. The nominal maxValue is 1, but higher values are allowed (no exception thrown). This parameter is a-rate.

Property of [apis/webaudio/GainNode](/apis/webaudio/GainNode)[apis/webaudio/GainNode](/apis/webaudio/GainNode)

## Syntax

``` js
var result = GainNode.gain;
GainNode.gain = value;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
var audioCtx = new AudioContext();
var gainNode = audioCtx.createGain();
gainNode.gain.value = 0.5;
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
