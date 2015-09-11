---
title: delayTime
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/DelayNode
    href: /apis/webaudio/DelayNode
standardization_status: 'W3C Editor''s Draft'
summary: 'An AudioParam object representing the amount of delay (in seconds) to apply. The default value (delayTime.value) is 0 (no delay). The minimum value is 0 and the maximum value is determined by the maxDelayTime argument to the AudioContext method createDelay. This parameter is k-rate.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/DelayNode/delayTime

---
## <span>Summary</span>

An AudioParam object representing the amount of delay (in seconds) to apply. The default value (delayTime.value) is 0 (no delay). The minimum value is 0 and the maximum value is determined by the maxDelayTime argument to the AudioContext method createDelay. This parameter is k-rate.

Property of [apis/webaudio/DelayNode](/apis/webaudio/DelayNode)[apis/webaudio/DelayNode](/apis/webaudio/DelayNode)

## <span>Syntax</span>

``` js
var result = DelayNode.delayTime;
DelayNode.delayTime = value;
```

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var myDelay = audioCtx.createDelay(5.0);
myDelay.delayTime.value = 3.0;
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
