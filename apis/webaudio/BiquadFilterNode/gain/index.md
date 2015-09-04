---
title: gain
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Used in different ways by the various types. Defaults to 0, with a nominal range of -40 to 40. This parameter is k-rate.'
uri: apis/webaudio/BiquadFilterNode/gain

---
# gain

## Summary

Used in different ways by the various types. Defaults to 0, with a nominal range of -40 to 40. This parameter is k-rate.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/BiquadFilterNode](/apis/webaudio/BiquadFilterNode)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = BiquadFilterNode.gain;
```

## Examples

``` {.js}
var audioCtx = new AudioContext();
var biquadFilter = audioCtx.createBiquadFilter();
biquadfilter.gain.value = 25;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

