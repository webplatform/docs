---
title: numberOfChannels
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Not Ready'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Not in spec; deletion candidate. Possibly confused with AudioBuffer/numberOfChannels.'
summary: "The number of channels of the destination's input. This value will default to 2, and may be set to any non-zero value less than or equal to maxChannelCount. An exception will be thrown if this value is not within the valid range.\n"
uri: apis/webaudio/AudioDestinationNode/numberOfChannels

---
# numberOfChannels

## Summary

The number of channels of the destination's input. This value will default to 2, and may be set to any non-zero value less than or equal to maxChannelCount. An exception will be thrown if this value is not within the valid range.

**Not in spec; deletion candidate. Possibly confused with AudioBuffer/numberOfChannels. See [http://webaudio.github.io/web-audio-api/](http://webaudio.github.io/web-audio-api/).**

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioDestinationNode](/apis/webaudio/AudioDestinationNode)</span></span>

## Syntax

``` {.js}
var result = AudioDestinationNode.numberOfChannels;
AudioDestinationNode.numberOfChannels = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

