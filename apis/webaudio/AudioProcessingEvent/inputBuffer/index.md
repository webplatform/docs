---
title: inputBuffer
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Out of Date'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Deprecated; deletion candidate. See http://webaudio.github.io/web-audio-api/.'
summary: "An AudioBuffer containing the input audio data. It will have a number of channels equal to the numberOfInputChannels parameter of the createScriptProcessor() method. This AudioBuffer is only valid while in the scope of the onaudioprocess function. Its values will be meaningless outside of this scope.\n"
uri: apis/webaudio/AudioProcessingEvent/inputBuffer

---
# inputBuffer

## Summary

An AudioBuffer containing the input audio data. It will have a number of channels equal to the numberOfInputChannels parameter of the createScriptProcessor() method. This AudioBuffer is only valid while in the scope of the onaudioprocess function. Its values will be meaningless outside of this scope.

**Deprecated; deletion candidate. See [http://webaudio.github.io/web-audio-api/](http://webaudio.github.io/web-audio-api/).**

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioProcessingEvent](/apis/webaudio/AudioProcessingEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioProcessingEvent.inputBuffer;
```

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

