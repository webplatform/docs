---
title: 'maxDecibels'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AnalyserNode
    href: /apis/webaudio/AnalyserNode
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/webaudio/AnalyserNode
standardization_status: 'W3C Editor''s Draft'
summary: 'The maximum power value in the scaling range for the FFT analysis data for conversion to unsigned byte values.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AnalyserNode/maxDecibels

---
## Summary

The maximum power value in the scaling range for the FFT analysis data for conversion to unsigned byte values.

Property of [apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)[apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)

## Syntax

``` js
var result = AnalyserNode.maxDecibels;
AnalyserNode.maxDecibels = value;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
analyser.maxDecibels = -10;
```

## Related specifications

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
