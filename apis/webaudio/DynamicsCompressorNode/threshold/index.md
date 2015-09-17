---
title: 'threshold'
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
summary: 'The decibel value above which the compression will start taking effect. Its default value is -24, with a nominal range of -100 to 0. This parameter is k-rate.'
tags:
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/DynamicsCompressorNode/threshold

---
## Summary

The decibel value above which the compression will start taking effect. Its default value is -24, with a nominal range of -100 to 0. This parameter is k-rate.

Property of [apis/webaudio/DynamicsCompressorNode](/apis/webaudio/DynamicsCompressorNode)[apis/webaudio/DynamicsCompressorNode](/apis/webaudio/DynamicsCompressorNode)

## Syntax

**Note**: This property is read-only.

``` js
var result = DynamicsCompressorNode.threshold;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
var audioCtx = new AudioContext();
var compressor = audioCtx.createDynamicsCompressor();
compressor.threshold.value = -50;
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
