---
title: GainNode
tags:
  0: API
  1: Objects
  3: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Changing the gain of an audio signal is a fundamental operation in audio applications. The GainNode is one of the building blocks for creating mixers. This interface is an AudioNode with a single input and single output, which multiplies the input audio signal by the (possibly time-varying) gain attribute, copying the result to the output.'
uri: apis/webaudio/GainNode

---
# GainNode

## Summary

Changing the gain of an audio signal is a fundamental operation in audio applications. The GainNode is one of the building blocks for creating mixers. This interface is an AudioNode with a single input and single output, which multiplies the input audio signal by the (possibly time-varying) gain attribute, copying the result to the output.

## Properties

API Name
:   Summary
[gain](/apis/webaudio/GainNode/gain)
:   Represents the amount of gain to apply. Its default value is 1 (no gain change). The nominal minValue is 0, but may be set negative for phase inversion. The nominal maxValue is 1, but higher values are allowed (no exception thrown). This parameter is a-rate.

## Methods

*No methods.*

## Events

*No events.*

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

