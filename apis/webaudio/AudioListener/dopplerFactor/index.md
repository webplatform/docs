---
title: dopplerFactor
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A constant used to determine the amount of pitch shift to use when rendering a doppler effect. The default value is 1.'
uri: apis/webaudio/AudioListener/dopplerFactor

---
# dopplerFactor

## Summary

A constant used to determine the amount of pitch shift to use when rendering a doppler effect. The default value is 1.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioListener](/apis/webaudio/AudioListener)</span></span>

## Syntax

``` {.js}
var result = AudioListener.dopplerFactor;
AudioListener.dopplerFactor = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var myListener = audioCtx.listener;
myListener.dopplerFactor = 1;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

