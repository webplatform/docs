---
title: defaultValue
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Initial value for the value attribute.'
uri: apis/webaudio/AudioParam/defaultValue

---
# defaultValue

## Summary

Initial value for the value attribute.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioParam](/apis/webaudio/AudioParam)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioParam.defaultValue;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var gainNode = audioCtx.createGain();
var gainDefault = gainNode.gain.defaultValue; //'gain' is the AudioParam
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

