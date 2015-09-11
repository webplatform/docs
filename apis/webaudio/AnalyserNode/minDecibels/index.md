---
title: minDecibels
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
summary: 'The minimum power value in the scaling range for the FFT analysis data for conversion to unsigned byte values. Default is -100.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AnalyserNode/minDecibels

---
## <span>Summary</span>

The minimum power value in the scaling range for the FFT analysis data for conversion to unsigned byte values. Default is -100.

Property of [apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)[apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)

## <span>Syntax</span>

``` js
var result = AnalyserNode.minDecibels;
AnalyserNode.minDecibels = value;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
analyser.minDecibels = -90;
```

## <span>Related specifications</span>

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
