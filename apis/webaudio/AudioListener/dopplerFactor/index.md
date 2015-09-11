---
title: dopplerFactor
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioListener
    href: /apis/webaudio/AudioListener
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/webaudio/AudioListener
standardization_status: 'W3C Editor''s Draft'
summary: 'A constant used to determine the amount of pitch shift to use when rendering a doppler effect. The default value is 1.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioListener/dopplerFactor

---
## <span>Summary</span>

A constant used to determine the amount of pitch shift to use when rendering a doppler effect. The default value is 1.

Property of [apis/webaudio/AudioListener](/apis/webaudio/AudioListener)[apis/webaudio/AudioListener](/apis/webaudio/AudioListener)

## <span>Syntax</span>

``` js
var result = AudioListener.dopplerFactor;
AudioListener.dopplerFactor = value;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var myListener = audioCtx.listener;
myListener.dopplerFactor = 1;
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
