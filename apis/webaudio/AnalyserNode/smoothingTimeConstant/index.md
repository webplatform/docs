---
title: smoothingTimeConstant
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A value from 0 to 1 representing the averaging constant with the last analysis frame. Default is 0.8.'
uri: apis/webaudio/AnalyserNode/smoothingTimeConstant

---
# smoothingTimeConstant

## Summary

A value from 0 to 1 representing the averaging constant with the last analysis frame. Default is 0.8.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)</span></span>

## Syntax

``` {.js}
var result = AnalyserNode.smoothingTimeConstant;
AnalyserNode.smoothingTimeConstant = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
analyser.smoothingTimeConstant = 1;
```

## Related specifications

Specification
:   Status
[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

