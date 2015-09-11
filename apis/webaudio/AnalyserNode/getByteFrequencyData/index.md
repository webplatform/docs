---
title: getByteFrequencyData
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
summary: 'Copies the current frequency data into the passed unsigned byte array. If the array has fewer elements than the frequencyBinCount, the excess elements will be dropped.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AnalyserNode/getByteFrequencyData

---
## <span>Summary</span>

Copies the current frequency data into the passed unsigned byte array. If the array has fewer elements than the frequencyBinCount, the excess elements will be dropped.

Method of [apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)[apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)

## <span>Syntax</span>

``` js
var  = AnalyserNode.getByteFrequencyData(array);
```

## <span>Parameters</span>

### <span>array</span>

 Data-type
:   void

 Where frequency-domain analysis data will be copied.

## <span>Return Value</span>

Returns an object of type<span></span>

Uint8Array

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
// Uint8Array should be the same length as the frequencyBinCount
var dataArray = new Uint8Array(analyser.frequencyBinCount);
// fill the Uint8Array with data returned from getByteFrequencyData()
analyser.getByteFrequencyData(myDataArray);
```

## <span>Related specifications</span>

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
