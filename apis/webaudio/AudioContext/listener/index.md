---
title: listener
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioContext
    href: /apis/webaudio/AudioContext
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/webaudio/AudioContext
standardization_status: 'W3C Editor''s Draft'
summary: 'An AudioListener, used for 3D spatialization.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioContext/listener

---
## Summary

An AudioListener, used for 3D spatialization.

Property of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

**Note**: This property is read-only.

``` js
var result = AudioContext.listener;
```

## Return Value

Returns an object of type

AudioListener

## Examples

``` js
var audioCtx = new AudioContext();
var myListener = audioCtx.listener;
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
