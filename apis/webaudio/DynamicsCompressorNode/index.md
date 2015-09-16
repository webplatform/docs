---
title: DynamicsCompressorNode
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'DynamicsCompressorNode is an AudioNode processor implementing a dynamics compression effect, which lowers the volume of the loudest parts of the signal and raises the volume of the softest parts. Compression is especially important in games and musical applications where large numbers of individual sounds are played simultaneously to control the overall signal level and help avoid clipping (distorting) the audio output to the speakers.'
tags:
  0: API
  1: Objects
  3: WebAudio
uri: apis/webaudio/DynamicsCompressorNode

---
## Summary

DynamicsCompressorNode is an AudioNode processor implementing a dynamics compression effect, which lowers the volume of the loudest parts of the signal and raises the volume of the softest parts. Compression is especially important in games and musical applications where large numbers of individual sounds are played simultaneously to control the overall signal level and help avoid clipping (distorting) the audio output to the speakers.

## Properties

API Name
:   Summary

[attack](/apis/webaudio/DynamicsCompressorNode/attack)
:   The amount of time (in seconds) to reduce the gain by 10dB. Its default value is 0.003, with a nominal range of 0 to 1. This parameter is k-rate.

[knee](/apis/webaudio/DynamicsCompressorNode/knee)
:   A decibel value representing the range above the threshold where the curve smoothly transitions to the *ratio* portion. Its default value is 30, with a nominal range of 0 to 40. This parameter is k-rate.

[ratio](/apis/webaudio/DynamicsCompressorNode/ratio)
:   The amount of dB change in input for a 1 dB change in output. Its default value is 12, with a nominal range of 1 to 20. This parameter is k-rate.

[reduction](/apis/webaudio/DynamicsCompressorNode/reduction)
:   A read-only decibel value for metering purposes, representing the current amount of gain reduction that the compressor is applying to the signal. If fed no signal the value will be 0 (no gain reduction). The nominal range is -20 to 0. This parameter is k-rate.

[release](/apis/webaudio/DynamicsCompressorNode/release)
:   The amount of time (in seconds) to increase the gain by 10dB. Its default value is 0.250, with a nominal range of 0 to 1. This parameter is k-rate.

[threshold](/apis/webaudio/DynamicsCompressorNode/threshold)
:   The decibel value above which the compression will start taking effect. Its default value is -24, with a nominal range of -100 to 0. This parameter is k-rate.

## Methods

*No methods.*

## Events

*No events.*

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
