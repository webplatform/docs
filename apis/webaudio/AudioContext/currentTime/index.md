---
title: currentTime
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'This is a time in seconds which starts at zero when the context is created and increases in real-time. All scheduled times are relative to it. This is not a transport time which can be started, paused, and re-positioned. It is always moving forward. A GarageBand-like timeline transport system can be very easily built on top of this (in JavaScript). This time corresponds to an ever-increasing hardware timestamp.'
uri: apis/webaudio/AudioContext/currentTime

---
# currentTime

## Summary

This is a time in seconds which starts at zero when the context is created and increases in real-time. All scheduled times are relative to it. This is not a transport time which can be started, paused, and re-positioned. It is always moving forward. A GarageBand-like timeline transport system can be very easily built on top of this (in JavaScript). This time corresponds to an ever-increasing hardware timestamp.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioContext.currentTime;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var ct = audioCtx.currentTime;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

