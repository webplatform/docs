---
title: 'release'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/DynamicsCompressorNode
    href: /apis/webaudio/DynamicsCompressorNode
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/webaudio/DynamicsCompressorNode
standardization_status: 'W3C Editor''s Draft'
summary: 'The amount of time (in seconds) to increase the gain by 10dB. Its default value is 0.250, with a nominal range of 0 to 1. This parameter is k-rate.'
tags:
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/DynamicsCompressorNode/release

---
## Summary

The amount of time (in seconds) to increase the gain by 10dB. Its default value is 0.250, with a nominal range of 0 to 1. This parameter is k-rate.

Property of [apis/webaudio/DynamicsCompressorNode](/apis/webaudio/DynamicsCompressorNode)[apis/webaudio/DynamicsCompressorNode](/apis/webaudio/DynamicsCompressorNode)

## Syntax

**Note**: This property is read-only.

``` js
var result = DynamicsCompressorNode.release;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
var audioCtx = new AudioContext();
var compressor = audioCtx.createDynamicsCompressor();
compressor.release.value = 0.25;
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
