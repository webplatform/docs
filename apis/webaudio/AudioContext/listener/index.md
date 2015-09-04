---
title: listener
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'An AudioListener, used for 3D spatialization.'
uri: apis/webaudio/AudioContext/listener

---
# listener

## Summary

An AudioListener, used for 3D spatialization.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioContext.listener;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

AudioListener

## Examples

``` {.js}
var audioCtx = new AudioContext();
var myListener = audioCtx.listener;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

