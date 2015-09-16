---
title: frequency
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/BiquadFilterNode
    href: /apis/webaudio/BiquadFilterNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Used in different ways by the various types. Defaults to 350Hz, with a nominal range of 10 to the Nyquist frequency (half the sample-rate). This parameter is k-rate.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/BiquadFilterNode/frequency

---
## Summary

Used in different ways by the various types. Defaults to 350Hz, with a nominal range of 10 to the Nyquist frequency (half the sample-rate). This parameter is k-rate.

Property of [apis/webaudio/BiquadFilterNode](/apis/webaudio/BiquadFilterNode)[apis/webaudio/BiquadFilterNode](/apis/webaudio/BiquadFilterNode)

## Syntax

**Note**: This property is read-only.

``` js
var result = BiquadFilterNode.frequency;
```

## Examples

``` js
var audioCtx = new AudioContext();
var biquadFilter = audioCtx.createBiquadFilter();
biquadfilter.frequency.value = 3000;
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
