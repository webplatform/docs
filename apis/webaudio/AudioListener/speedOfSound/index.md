---
title: 'speedOfSound'
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
summary: 'The speed of sound used for calculating doppler shift. The default value is 343.3 meters / second.'
tags:
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/AudioListener/speedOfSound

---
## Summary

The speed of sound used for calculating doppler shift. The default value is 343.3 meters / second.

Property of [apis/webaudio/AudioListener](/apis/webaudio/AudioListener)[apis/webaudio/AudioListener](/apis/webaudio/AudioListener)

## Syntax

``` js
var result = AudioListener.speedOfSound;
AudioListener.speedOfSound = value;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
var audioCtx = new AudioContext();
var myListener = audioCtx.listener;
myListener.speedOfSound = 343.3;
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
