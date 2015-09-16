---
title: 'AnalyserNode'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'This interface represents a node which is able to provide real-time frequency and time-domain analysis information. The audio stream will be passed un-processed from input to output.'
tags:
  0: API
  1: Objects
  3: WebAudio
uri: apis/webaudio/AnalyserNode

---
## Summary

This interface represents a node which is able to provide real-time frequency and time-domain analysis information. The audio stream will be passed un-processed from input to output.

## Properties

API Name
:   Summary

[fftSize](/apis/webaudio/AnalyserNode/fftSize)
:   The size of the FFT (Fast Fourier Transform) used for frequency-domain analysis. Must be a power of two in the range 32-2048; defaults to 2048.

[frequencyBinCount](/apis/webaudio/AnalyserNode/frequencyBinCount)
:   Half the [fftSize](/apis/webaudio/AnalyserNode/fftSize) (the size of the FFT used for frequency-domain analysis).

[maxDecibels](/apis/webaudio/AnalyserNode/maxDecibels)
:   The maximum power value in the scaling range for the FFT analysis data for conversion to unsigned byte values.

[minDecibels](/apis/webaudio/AnalyserNode/minDecibels)
:   The minimum power value in the scaling range for the FFT analysis data for conversion to unsigned byte values. Default is -100.

[smoothingTimeConstant](/apis/webaudio/AnalyserNode/smoothingTimeConstant)
:   A value from 0 to 1 representing the averaging constant with the last analysis frame. Default is 0.8.

## Methods

API Name
:   Summary

[getByteFrequencyData](/apis/webaudio/AnalyserNode/getByteFrequencyData)
:   Copies the current frequency data into the passed unsigned byte array. If the array has fewer elements than the [frequencyBinCount](/apis/webaudio/AnalyserNode/frequencyBinCount), the excess elements will be dropped.

[getByteTimeDomainData](/apis/webaudio/AnalyserNode/getByteTimeDomainData)
:   Copies the current time-domain (waveform) data into the passed unsigned byte array. If the array has fewer elements than the [frequencyBinCount](/apis/webaudio/AnalyserNode/frequencyBinCount), the excess elements will be dropped.

[getFloatFrequencyData](/apis/webaudio/AnalyserNode/getFloatFrequencyData)
:   Copies the current frequency data into the passed floating-point array. If the array has fewer elements than the [**frequencyBinCount**](/apis/webaudio/AnalyserNode/frequencyBinCount), the excess elements will be dropped.

## Events

*No events.*

## Related specifications

[W3C Web Audio API](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html)
:   W3C Editor's Draft
