---
title: computedValue
notes:
  - 'Not in spec; deletion candidate. See http://webaudio.github.io/web-audio-api/.'
readiness: 'Not Ready'
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
summary: "The final value controlling the audio DSP, calculated at each time, which is either the value set directly to the value attribute or, if there are any scheduled parameter changes (automation events), the value as calculated from these events.\n"
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioParam/computedValue

---
## <span>Summary</span>

The final value controlling the audio DSP, calculated at each time, which is either the value set directly to the value attribute or, if there are any scheduled parameter changes (automation events), the value as calculated from these events.

**Not in spec; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

Property of [apis/webaudio/AudioParam](/apis/webaudio/AudioParam)[apis/webaudio/AudioParam](/apis/webaudio/AudioParam)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = AudioParam.computedValue;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
