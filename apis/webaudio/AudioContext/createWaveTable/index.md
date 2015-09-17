---
title: 'createWaveTable'
notes:
  - 'Out of date; removed from spec. See http://webaudio.github.io/web-audio-api/.'
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/AudioContext
    href: /apis/webaudio/AudioContext
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/webaudio/AudioContext
standardization_status: 'W3C Editor''s Draft'
summary: "Creates a WaveTable representing a waveform containing arbitrary harmonic content. The real and imag parameters must be of type Float32Array of equal lengths greater than zero and less than or equal to 4096 or an exception will be thrown. These parameters specify the Fourier coefficients of a Fourier series representing the partials of a periodic waveform. The created WaveTable will be used with an OscillatorNode and will represent a normalized time-domain waveform having maximum absolute peak value of 1. Another way of saying this is that the generated waveform of an OscillatorNode will have maximum peak value at 0dBFS. Conveniently, this corresponds to the full-range of the signal values used by the Web Audio API. Because the WaveTable will be normalized on creation, the real and imag parameters represent relative values.\n"
tags:
  - API_Object_Methods
  - API
  - WebAudio
  - Needs_Examples
uri: apis/webaudio/AudioContext/createWaveTable

---
## Summary

Creates a WaveTable representing a waveform containing arbitrary harmonic content. The real and imag parameters must be of type Float32Array of equal lengths greater than zero and less than or equal to 4096 or an exception will be thrown. These parameters specify the Fourier coefficients of a Fourier series representing the partials of a periodic waveform. The created WaveTable will be used with an OscillatorNode and will represent a normalized time-domain waveform having maximum absolute peak value of 1. Another way of saying this is that the generated waveform of an OscillatorNode will have maximum peak value at 0dBFS. Conveniently, this corresponds to the full-range of the signal values used by the Web Audio API. Because the WaveTable will be normalized on creation, the real and imag parameters represent relative values.

**Out of date; removed from spec. See <http://webaudio.github.io/web-audio-api/>.**

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

``` js
var  = AudioContext.createWaveTable(real, imag);
```

## Parameters

### real

 Data-type
:   String

 Represents an array of cosine terms (traditionally the A terms). In audio terminology, the first element (index 0) is the DC-offset of the periodic waveform and is usually set to zero. The second element (index 1) represents the fundamental frequency. The third element represents the first overtone, and so on.

### imag

 Data-type
:   String

 Represents an array of sine terms (traditionally the B terms). The first element (index 0) should be set to zero (and will be ignored) since this term does not exist in the Fourier series. The second element (index 1) represents the fundamental frequency. The third element represents the first overtone, and so on.

## Return Value

Returns an object of type

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
