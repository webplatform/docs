---
title: createBiquadFilter
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Creates a BiquadFilterNode representing a second order filter which can be configured as one of several common filter types.'
uri: apis/webaudio/AudioContext/createBiquadFilter

---
# createBiquadFilter

## Summary

Creates a BiquadFilterNode representing a second order filter which can be configured as one of several common filter types.

*Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)*

## Syntax

``` {.js}
var  = AudioContext.createBiquadFilter();
```

## Return Value

Returns an object of type .

BiquadFilter

## Examples

``` {.js}
var audioCtx = new AudioContext();
var biquadFilter = audioCtx.createBiquadFilter();
```

## Related specifications

Specification
:   Status
[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

