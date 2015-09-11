---
title: currentTime
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioContext
    href: /apis/webaudio/AudioContext
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/webaudio/AudioContext
standardization_status: 'W3C Editor''s Draft'
summary: 'This is a time in seconds which starts at zero when the context is created and increases in real-time. All scheduled times are relative to it. This is not a transport time which can be started, paused, and re-positioned. It is always moving forward. A GarageBand-like timeline transport system can be very easily built on top of this (in JavaScript). This time corresponds to an ever-increasing hardware timestamp.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioContext/currentTime

---
## <span>Summary</span>

This is a time in seconds which starts at zero when the context is created and increases in real-time. All scheduled times are relative to it. This is not a transport time which can be started, paused, and re-positioned. It is always moving forward. A GarageBand-like timeline transport system can be very easily built on top of this (in JavaScript). This time corresponds to an ever-increasing hardware timestamp.

Property of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = AudioContext.currentTime;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var ct = audioCtx.currentTime;
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
