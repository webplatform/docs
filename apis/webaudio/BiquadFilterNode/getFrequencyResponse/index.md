---
title: getFrequencyResponse
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/BiquadFilterNode
    href: /apis/webaudio/BiquadFilterNode
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/webaudio/BiquadFilterNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Given the current filter parameter settings, calculates the frequency response for the specified frequencies.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/BiquadFilterNode/getFrequencyResponse

---
## <span>Summary</span>

Given the current filter parameter settings, calculates the frequency response for the specified frequencies.

Method of [apis/webaudio/BiquadFilterNode](/apis/webaudio/BiquadFilterNode)[apis/webaudio/BiquadFilterNode](/apis/webaudio/BiquadFilterNode)

## <span>Syntax</span>

``` js
var  = BiquadFilterNode.getFrequencyResponse(frequencyHz, magResponse, phaseResponse);
```

## <span>Parameters</span>

### <span>frequencyHz</span>

 Data-type
:   void

 Specifies an array of frequencies at which the response values will be calculated.

### <span>magResponse</span>

 Data-type
:   void

 Specifies an output array receiving the linear magnitude response values.

### <span>phaseResponse</span>

 Data-type
:   void

 Specifies an output array receiving the phase response values in radians.

## <span>Return Value</span>

Returns an object of type<span></span>

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var biquadFilter = audioCtx.createBiquadFilter();
biquadfilter.getFrequencyResponse(myFrequencyArray,magResponseOutput,phaseResponseOutput);
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
