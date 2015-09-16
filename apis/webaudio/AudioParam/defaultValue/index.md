---
title: defaultValue
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioParam
    href: /apis/webaudio/AudioParam
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/webaudio/AudioParam
standardization_status: 'W3C Editor''s Draft'
summary: 'Initial value for the value attribute.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioParam/defaultValue

---
## Summary

Initial value for the value attribute.

Property of [apis/webaudio/AudioParam](/apis/webaudio/AudioParam)[apis/webaudio/AudioParam](/apis/webaudio/AudioParam)

## Syntax

**Note**: This property is read-only.

``` js
var result = AudioParam.defaultValue;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
var gainNode = audioCtx.createGain();
var gainDefault = gainNode.gain.defaultValue; //'gain' is the AudioParam
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
