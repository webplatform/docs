---
title: 'type'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/BiquadFilterNode
    href: /apis/webaudio/BiquadFilterNode
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned short'
    href: /apis/webaudio/BiquadFilterNode
standardization_status: 'W3C Editor''s Draft'
summary: 'The type of BiquadFilterNode (filtering algorithm) the node is implementing.'
tags:
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/BiquadFilterNode/type

---
## Summary

The type of BiquadFilterNode (filtering algorithm) the node is implementing.

Property of [apis/webaudio/BiquadFilterNode](/apis/webaudio/BiquadFilterNode)[apis/webaudio/BiquadFilterNode](/apis/webaudio/BiquadFilterNode)

## Syntax

``` js
var result = BiquadFilterNode.type;
BiquadFilterNode.type = value;
```

## Return Value

Returns an object of type unsigned shortunsigned short

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

``` js
var audioCtx = new AudioContext();
var biquadFilter = audioCtx.createBiquadFilter();
biquadfilter.type = 'lowpass';
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
