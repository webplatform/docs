---
title: gain
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/BiquadFilterNode
    href: /apis/webaudio/BiquadFilterNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Used in different ways by the various types. Defaults to 0, with a nominal range of -40 to 40. This parameter is k-rate.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/BiquadFilterNode/gain

---
## <span>Summary</span>

Used in different ways by the various types. Defaults to 0, with a nominal range of -40 to 40. This parameter is k-rate.

Property of [apis/webaudio/BiquadFilterNode](/apis/webaudio/BiquadFilterNode)[apis/webaudio/BiquadFilterNode](/apis/webaudio/BiquadFilterNode)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = BiquadFilterNode.gain;
```

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var biquadFilter = audioCtx.createBiquadFilter();
biquadfilter.gain.value = 25;
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
