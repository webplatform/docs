---
title: getByteFrequencyData
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Copies the current frequency data into the passed unsigned byte array. If the array has fewer elements than the frequencyBinCount, the excess elements will be dropped.'
uri: apis/webaudio/AnalyserNode/getByteFrequencyData

---
# getByteFrequencyData

## Summary

Copies the current frequency data into the passed unsigned byte array. If the array has fewer elements than the frequencyBinCount, the excess elements will be dropped.

*Method of [apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)*

## Syntax

``` {.js}
var  = AnalyserNode.getByteFrequencyData(array);
```

## Parameters

### array

 Data-typeÂ
:   void

 Where frequency-domain analysis data will be copied.

## Return Value

Returns an object of type .

Uint8Array

## Examples

``` {.js}
var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
// Uint8Array should be the same length as the frequencyBinCount
var dataArray = new Uint8Array(analyser.frequencyBinCount);
// fill the Uint8Array with data returned from getByteFrequencyData()
analyser.getByteFrequencyData(myDataArray);
```

## Related specifications

Specification
:   Status
[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

