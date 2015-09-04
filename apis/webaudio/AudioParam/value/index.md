---
title: value
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The parameter''s floating-point value. If a value is set outside the allowable range no exception is thrown, because these limits are nominal and may be exceeded. If a value is set during a time when there are any automation events scheduled then it will be ignored and no exception will be thrown.'
uri: apis/webaudio/AudioParam/value

---
# value

## Summary

The parameter's floating-point value. If a value is set outside the allowable range no exception is thrown, because these limits are nominal and may be exceeded. If a value is set during a time when there are any automation events scheduled then it will be ignored and no exception will be thrown.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioParam](/apis/webaudio/AudioParam)</span></span>

## Syntax

``` {.js}
var result = AudioParam.value;
AudioParam.value = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var gainNode = audioCtx.createGain();
gainNode.gain.value = 0; //'gain' is the AudioParam
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

## See also

### Related articles

#### Audio

-   [audio-video](/apis/audio-video)

-   [enabled](/apis/audio-video/AudioTrack/enabled)

-   [language](/apis/audio-video/AudioTrack/language)

-   [Web Audio API](/apis/webaudio)

-   **value**

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   [user-input](/css/properties/user-input)

-   [bgSound](/html/elements/bgSound)

-   [bgsound](/html/elements/bgSound/ja)

-   [implementing html5 audio](/tutorials/implementing_html5_audio)

-   [WebRTC Resources](/tutorials/webrtc_resources)

