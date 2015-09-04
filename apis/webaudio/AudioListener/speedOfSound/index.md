---
title: speedOfSound
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The speed of sound used for calculating doppler shift. The default value is 343.3 meters / second.'
uri: apis/webaudio/AudioListener/speedOfSound

---
# speedOfSound

## Summary

The speed of sound used for calculating doppler shift. The default value is 343.3 meters / second.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioListener](/apis/webaudio/AudioListener)</span></span>

## Syntax

``` {.js}
var result = AudioListener.speedOfSound;
AudioListener.speedOfSound = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var myListener = audioCtx.listener;
myListener.speedOfSound = 343.3;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

