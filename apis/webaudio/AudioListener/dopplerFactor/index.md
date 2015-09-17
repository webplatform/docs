---
title: 'dopplerFactor'
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
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/AudioListener/dopplerFactor

---
## Summary

A constant used to determine the amount of pitch shift to use when rendering a doppler effect. The default value is 1.

Property of [apis/webaudio/AudioListener](/apis/webaudio/AudioListener)[apis/webaudio/AudioListener](/apis/webaudio/AudioListener)

## Syntax

``` js
var result = AudioListener.dopplerFactor;
AudioListener.dopplerFactor = value;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
var audioCtx = new AudioContext();
var myListener = audioCtx.listener;
myListener.dopplerFactor = 1;
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
