---
title: outputBuffer
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Out of Date'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Deprecated; deletion candidate. See http://webaudio.github.io/web-audio-api/.'
summary: "An AudioBuffer where the output audio data should be written. It will have a number of channels equal to the numberOfOutputChannels parameter of the createScriptProcessor() method. Script code within the scope of the onaudioprocess function is expected to modify the Float32Array arrays representing channel data in this AudioBuffer. Any script modifications to this AudioBuffer outside of this scope will not produce any audible effects.\n"
uri: apis/webaudio/AudioProcessingEvent/outputBuffer

---
# outputBuffer

## Summary

An AudioBuffer where the output audio data should be written. It will have a number of channels equal to the numberOfOutputChannels parameter of the createScriptProcessor() method. Script code within the scope of the onaudioprocess function is expected to modify the Float32Array arrays representing channel data in this AudioBuffer. Any script modifications to this AudioBuffer outside of this scope will not produce any audible effects.

**Deprecated; deletion candidate. See [http://webaudio.github.io/web-audio-api/](http://webaudio.github.io/web-audio-api/).**

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioProcessingEvent](/apis/webaudio/AudioProcessingEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioProcessingEvent.outputBuffer;
```

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

