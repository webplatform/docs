---
title: outputBuffer
notes:
  - 'Deprecated; deletion candidate. See http://webaudio.github.io/web-audio-api/.'
readiness: 'Out of Date'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioProcessingEvent
    href: /apis/webaudio/AudioProcessingEvent
standardization_status: 'W3C Editor''s Draft'
summary: "An AudioBuffer where the output audio data should be written. It will have a number of channels equal to the numberOfOutputChannels parameter of the createScriptProcessor() method. Script code within the scope of the onaudioprocess function is expected to modify the Float32Array arrays representing channel data in this AudioBuffer. Any script modifications to this AudioBuffer outside of this scope will not produce any audible effects.\n"
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioProcessingEvent/outputBuffer

---
## Summary

An AudioBuffer where the output audio data should be written. It will have a number of channels equal to the numberOfOutputChannels parameter of the createScriptProcessor() method. Script code within the scope of the onaudioprocess function is expected to modify the Float32Array arrays representing channel data in this AudioBuffer. Any script modifications to this AudioBuffer outside of this scope will not produce any audible effects.

**Deprecated; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

Property of [apis/webaudio/AudioProcessingEvent](/apis/webaudio/AudioProcessingEvent)[apis/webaudio/AudioProcessingEvent](/apis/webaudio/AudioProcessingEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = AudioProcessingEvent.outputBuffer;
```

**Needs Examples**: This section should include examples.

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
