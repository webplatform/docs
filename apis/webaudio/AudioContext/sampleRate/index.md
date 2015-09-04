---
title: sampleRate
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The sample rate, in sample-frames per second, at which the AudioContext handles audio. It is assumed that all AudioNodes in the context run at this rate. In making this assumption, sample-rate converters or varispeed processors are not supported in real-time processing.'
uri: apis/webaudio/AudioContext/sampleRate

---
# sampleRate

## Summary

The sample rate, in sample-frames per second, at which the AudioContext handles audio. It is assumed that all AudioNodes in the context run at this rate. In making this assumption, sample-rate converters or varispeed processors are not supported in real-time processing.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioContext.sampleRate;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var mySampleRate = audioCtx.sampleRate;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

