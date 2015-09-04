---
title: getByteTimeDomainData
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Copies the current time-domain (waveform) data into the passed unsigned byte array. If the array has fewer elements than the frequencyBinCount, the excess elements will be dropped.'
uri: apis/webaudio/AnalyserNode/getByteTimeDomainData

---
# getByteTimeDomainData

## Summary

Copies the current time-domain (waveform) data into the passed unsigned byte array. If the array has fewer elements than the frequencyBinCount, the excess elements will be dropped.

*Method of [apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)*

## Syntax

``` {.js}
var  = AnalyserNode.getByteTimeDomainData(array);
```

## Parameters

### array

 Data-typeÂ
:   void

 Were time-domain analysis data will be copied.

## Return Value

Returns an object of type .

Uint8Array

## Examples

``` {.js}
var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
// Uint8Array should be the same length as the fftSize
var dataArray = new Uint8Array(analyser.fftSize);
// fill the Uint8Array with data returned from getByteTimeDomainData()
analyser.getByteTimeDomainData(myDataArray);
```

## Related specifications

Specification
:   Status
[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

