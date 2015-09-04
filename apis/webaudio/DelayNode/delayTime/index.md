---
title: delayTime
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'An AudioParam object representing the amount of delay (in seconds) to apply. The default value (delayTime.value) is 0 (no delay). The minimum value is 0 and the maximum value is determined by the maxDelayTime argument to the AudioContext method createDelay. This parameter is k-rate.'
uri: apis/webaudio/DelayNode/delayTime

---
# delayTime

## Summary

An AudioParam object representing the amount of delay (in seconds) to apply. The default value (delayTime.value) is 0 (no delay). The minimum value is 0 and the maximum value is determined by the maxDelayTime argument to the AudioContext method createDelay. This parameter is k-rate.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/DelayNode](/apis/webaudio/DelayNode)</span></span>

## Syntax

``` {.js}
var result = DelayNode.delayTime;
DelayNode.delayTime = value;
```

## Examples

``` {.js}
var audioCtx = new AudioContext();
var myDelay = audioCtx.createDelay(5.0);
myDelay.delayTime.value = 3.0;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

