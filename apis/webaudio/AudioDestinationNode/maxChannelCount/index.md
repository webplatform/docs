---
title: maxChannelCount
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The maximum number of channels that the physical hardware is capable of supporting. The AudioNode channelCount property can be set between 0 and this value, inclusive. A value of 0 indicates that the channel count may not be changed. Default is 2.'
uri: apis/webaudio/AudioDestinationNode/maxChannelCount

---
# maxChannelCount

## Summary

The maximum number of channels that the physical hardware is capable of supporting. The AudioNode channelCount property can be set between 0 and this value, inclusive. A value of 0 indicates that the channel count may not be changed. Default is 2.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioDestinationNode](/apis/webaudio/AudioDestinationNode)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioDestinationNode.maxChannelCount;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var myDestination = audioCtx.destination;
mcc = myDestination.maxChannelCount;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

