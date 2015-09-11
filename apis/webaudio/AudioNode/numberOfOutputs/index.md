---
title: numberOfOutputs
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioNode
    href: /apis/webaudio/AudioNode
standardization_status: 'W3C Editor''s Draft'
summary: 'The number of outputs coming out of an AudioNode. For destination nodes, this will be 0.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioNode/numberOfOutputs

---
## <span>Summary</span>

The number of outputs coming out of an AudioNode. For destination nodes, this will be 0.

Property of [apis/webaudio/AudioNode](/apis/webaudio/AudioNode)[apis/webaudio/AudioNode](/apis/webaudio/AudioNode)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = AudioNode.numberOfOutputs;
```

## <span>Examples</span>

``` js
var oscillator = audioCtx.createOscillator();
var outputs = oscillator.numberOfOutputs;
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
