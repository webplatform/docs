---
title: 'delayTime'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/DelayNode
    href: /apis/webaudio/DelayNode
standardization_status: 'W3C Editor''s Draft'
summary: 'An AudioParam object representing the amount of delay (in seconds) to apply. The default value (delayTime.value) is 0 (no delay). The minimum value is 0 and the maximum value is determined by the maxDelayTime argument to the AudioContext method createDelay. This parameter is k-rate.'
tags:
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/DelayNode/delayTime

---
## Summary

An AudioParam object representing the amount of delay (in seconds) to apply. The default value (delayTime.value) is 0 (no delay). The minimum value is 0 and the maximum value is determined by the maxDelayTime argument to the AudioContext method createDelay. This parameter is k-rate.

Property of [apis/webaudio/DelayNode](/apis/webaudio/DelayNode)[apis/webaudio/DelayNode](/apis/webaudio/DelayNode)

## Syntax

``` js
var result = DelayNode.delayTime;
DelayNode.delayTime = value;
```

## Examples

``` js
var audioCtx = new AudioContext();
var myDelay = audioCtx.createDelay(5.0);
myDelay.delayTime.value = 3.0;
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
