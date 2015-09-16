---
title: 'BiquadFilterNode'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'BiquadFilterNode is an AudioNode processor implementing common low-order filters, which are the building blocks of basic tone controls (bass, mid, treble), graphic equalizers, and more advanced filters. Multiple BiquadFilterNode filters can be combined to form more complex filters. Each BiquadFilterNode can be configured as one of a number of common filter types as listed in the type property page, linked below. The default filter type is LOWPASS.'
tags:
  0: API
  1: Objects
  3: WebAudio
uri: apis/webaudio/BiquadFilterNode

---
## Summary

BiquadFilterNode is an AudioNode processor implementing common low-order filters, which are the building blocks of basic tone controls (bass, mid, treble), graphic equalizers, and more advanced filters. Multiple BiquadFilterNode filters can be combined to form more complex filters. Each BiquadFilterNode can be configured as one of a number of common filter types as listed in the type property page, linked below. The default filter type is LOWPASS.

## Properties

API Name
:   Summary

[Q](/apis/webaudio/BiquadFilterNode/Q)
:   Used in different ways by the various types. Defaults to 1, with a nominal range of 0.0001 to 1000. This parameter is k-rate.

[frequency](/apis/webaudio/BiquadFilterNode/frequency)
:   Used in different ways by the various types. Defaults to 350Hz, with a nominal range of 10 to the Nyquist frequency (half the sample-rate). This parameter is k-rate.

[gain](/apis/webaudio/BiquadFilterNode/gain)
:   Used in different ways by the various types. Defaults to 0, with a nominal range of -40 to 40. This parameter is k-rate.

[type](/apis/webaudio/BiquadFilterNode/type)
:   The type of ****BiquadFilterNode**** (filtering algorithm) the node is implementing.

## Methods

API Name
:   Summary

[getFrequencyResponse](/apis/webaudio/BiquadFilterNode/getFrequencyResponse)
:   Given the current filter parameter settings, calculates the frequency response for the specified frequencies.

## Events

*No events.*

## Related specifications

[W3C Web Audio API](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html)
:   W3C Editor's Draft
