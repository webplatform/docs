---
title: computedValue
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Not Ready'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Not in spec; deletion candidate. See http://webaudio.github.io/web-audio-api/.'
summary: "The final value controlling the audio DSP, calculated at each time, which is either the value set directly to the value attribute or, if there are any scheduled parameter changes (automation events), the value as calculated from these events.\n"
uri: apis/webaudio/AudioParam/computedValue

---
# computedValue

## Summary

The final value controlling the audio DSP, calculated at each time, which is either the value set directly to the value attribute or, if there are any scheduled parameter changes (automation events), the value as calculated from these events.

**Not in spec; deletion candidate. See [http://webaudio.github.io/web-audio-api/](http://webaudio.github.io/web-audio-api/).**

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioParam](/apis/webaudio/AudioParam)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioParam.computedValue;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

