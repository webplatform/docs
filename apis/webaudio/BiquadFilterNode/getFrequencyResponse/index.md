---
title: getFrequencyResponse
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Given the current filter parameter settings, calculates the frequency response for the specified frequencies.'
uri: apis/webaudio/BiquadFilterNode/getFrequencyResponse

---
# getFrequencyResponse

## Summary

Given the current filter parameter settings, calculates the frequency response for the specified frequencies.

*Method of [apis/webaudio/BiquadFilterNode](/apis/webaudio/BiquadFilterNode)*

## Syntax

``` {.js}
var  = BiquadFilterNode.getFrequencyResponse(frequencyHz, magResponse, phaseResponse);
```

## Parameters

### frequencyHz

 Data-typeÂ
:   void

 Specifies an array of frequencies at which the response values will be calculated.

### magResponse

 Data-typeÂ
:   void

 Specifies an output array receiving the linear magnitude response values.

### phaseResponse

 Data-typeÂ
:   void

 Specifies an output array receiving the phase response values in radians.

## Return Value

Returns an object of type .

## Examples

``` {.js}
var audioCtx = new AudioContext();
var biquadFilter = audioCtx.createBiquadFilter();
biquadfilter.getFrequencyResponse(myFrequencyArray,magResponseOutput,phaseResponseOutput);
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

