---
title: type
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The type of BiquadFilterNode (filtering algorithm) the node is implementing.'
uri: apis/webaudio/BiquadFilterNode/type

---
# type

## Summary

The type of BiquadFilterNode (filtering algorithm) the node is implementing.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/BiquadFilterNode](/apis/webaudio/BiquadFilterNode)</span></span>

## Syntax

``` {.js}
var result = BiquadFilterNode.type;
BiquadFilterNode.type = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned short</span></span>

Uses one of the following constant values:

-   LOWPASS (0) (default), a standard second-order resonant lowpass filter with 12dB/octave rolloff;
-   HIGHPASS (1), a standard second-order resonant highpass filter with 12dB/octave rolloff;
-   BANDPASS (2), a second-order bandpass filter;
-   LOWSHELF (3), a second-order lowshelf filter;
-   HIGHSHELF (4), a second-order highshelf filter;
-   PEAKING (5), a boost (or attenuation) to a range of frequencies;
-   NOTCH (6), restricting a set of frequencies;
-   ALLPASS (7), a second-order allpass filter.

## Examples

``` {.js}
var audioCtx = new AudioContext();
var biquadFilter = audioCtx.createBiquadFilter();
biquadfilter.type = 'lowpass';
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

