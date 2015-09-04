---
title: bgSound
tags:
  - Pages
  - using
  - duplicate
  - arguments
  - in
  - template
  - calls
  - Markup
  - Elements
  - HTML
readiness: 'Not Ready'
standardization_status: Non-Standard
notes:
  - 'Deletion Candidate: It''s deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features'
summary: 'The bgsound element (<bgsound>) instructs the browser to load and play a sound file while the user is on that page. Don''t use it. Use the audio element instead.'
uri: html/elements/bgSound

---
# bgSound

## Summary

The bgsound element (\<bgsound\>) instructs the browser to load and play a sound file while the user is on that page. Don't use it. Use the audio element instead.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLBGSoundElement](/dom/HTMLBGSoundElement)

## Examples

If you want to use sound, please use the [audio](/html/elements/audio) element:

``` {.html}


<audio autoplay id="bgsound">
 <source src="http://media.w3.org/2010/07/bunny/04-Death_Becomes_Fur.mp4"
         type="audio/mp4">
 <source src="http://media.w3.org/2010/07/bunny/04-Death_Becomes_Fur.oga"
         type="audio/ogg; codecs=vorbis">
 <p>Your user agent does not support the HTML5 Audio element.</p>
</audio>
<button type="button"
        onclick="document.getElementById('bgsound').pause();">
  Stop background sound
</button>
```

</pre>

## Notes

### Remarks

The `<bgSound>` element can appear anywhere within the document. This element is not rendered. This element does not require a closing tag. Do not use it! In HTML5 the `<bgSound>` is described as ["non-conforming feature"](http://www.w3.org/TR/html5/obsolete.html#non-conforming-features).

### Standards information

There are no standards that apply here.

### HTML information

{

## See also

### Related articles

#### Audio

-   [audio-video](/apis/audio-video)

-   [enabled](/apis/audio-video/AudioTrack/enabled)

-   [language](/apis/audio-video/AudioTrack/language)

-   [Web Audio API](/apis/webaudio)

-   [value](/apis/webaudio/AudioParam/value)

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   [user-input](/css/properties/user-input)

-   **bgSound**

-   [bgsound](/html/elements/bgSound/ja)

-   [implementing html5 audio](/tutorials/implementing_html5_audio)

-   [WebRTC Resources](/tutorials/webrtc_resources)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

