---
title: 'getFloatFrequencyData'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/AnalyserNode
    href: /apis/webaudio/AnalyserNode
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/webaudio/AnalyserNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Copies the current frequency data into the passed floating-point array. If the array has fewer elements than the frequencyBinCount, the excess elements will be dropped.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AnalyserNode/getFloatFrequencyData

---
## Summary

Copies the current frequency data into the passed floating-point array. If the array has fewer elements than the frequencyBinCount, the excess elements will be dropped.

Method of [apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)[apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)

## Syntax

``` js
var  = AnalyserNode.getFloatFrequencyData(array);
```

## Parameters

### array

 Data-type
:   void

 Where frequency-domain analysis data will be copied.

## Return Value

Returns an object of type

Float32Array

## Examples

``` js
var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
// Float32Array should be the same length as the frequencyBinCount
var myDataArray = new Float32Array(analyser.frequencyBinCount);
// fill the Float32Array with data returned from getFloatFrequencyData()
analyser.getFloatFrequencyData(myDataArray);
```

## Related specifications

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
