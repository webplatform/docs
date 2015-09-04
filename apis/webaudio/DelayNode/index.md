---
title: DelayNode
tags:
  0: API
  1: Objects
  3: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A delay-line is a fundamental building block in audio applications. This interface is an AudioNode with a single input and single output, which delays the incoming audio signal by a certain amount. The default amount is 0 seconds (no delay).'
uri: apis/webaudio/DelayNode

---
# DelayNode

## Summary

A delay-line is a fundamental building block in audio applications. This interface is an AudioNode with a single input and single output, which delays the incoming audio signal by a certain amount. The default amount is 0 seconds (no delay).

## Properties

API Name
:   Summary
[delayTime](/apis/webaudio/DelayNode/delayTime)
:   An [**AudioParam**](/apis/webaudio/AudioParam) object representing the amount of delay (in seconds) to apply. The default value (delayTime.value) is 0 (no delay). The minimum value is 0 and the maximum value is determined by the **maxDelayTime** argument to the [**AudioContext**](/apis/webaudio/AudioContext) method [**createDelay**](/apis/webaudio/AudioContext/createDelay). This parameter is k-rate.

## Methods

*No methods.*

## Events

*No events.*

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

