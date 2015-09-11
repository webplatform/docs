---
title: smoothingTimeConstant
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
summary: 'A value from 0 to 1 representing the averaging constant with the last analysis frame. Default is 0.8.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AnalyserNode/smoothingTimeConstant

---
## <span>Summary</span>

A value from 0 to 1 representing the averaging constant with the last analysis frame. Default is 0.8.

Property of [apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)[apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)

## <span>Syntax</span>

``` js
var result = AnalyserNode.smoothingTimeConstant;
AnalyserNode.smoothingTimeConstant = value;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
analyser.smoothingTimeConstant = 1;
```

## <span>Related specifications</span>

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
