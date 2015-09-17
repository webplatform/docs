---
title: 'audio'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/HTML/Element/audio)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/7282145'
compatibility:
  feature: audio
  topic: html
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLAudioElement](/dom/HTMLAudioElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The audio element (&lt;audio&gt;) is used for playing audio files and may display a minimal media player user interface.'
tags:
  - Markup_Elements
  - Audio
  - HTML
  - Media
uri: html/elements/audio

---
## Summary

The audio element (&lt;audio&gt;) is used for playing audio files and may display a minimal media player user interface.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLAudioElement](/dom/HTMLAudioElement)

Extensive documentation on manipulating the element may be found on the [HTMLAudioElement](/dom/HTMLAudioElement) page.

## HTML Attributes

-   `autoplay` = "autoplay" or "" (empty string) or empty
    Instructs the UA to automatically begin playback of the audio stream as soon as it can do so without stopping.
-   `preload` = "none" or "metadata" or "auto" or "" (empty string) or empty
    Represents a hint to the UA about whether optimistic downloading of the audio stream itself or its metadata is considered worthwhile.
    -   "none": Hints to the UA that the user is not expected to need the video, or that minimizing unnecessary traffic is desirable.
    -   "metadata": Hints to the UA that the user is not expected to need the audio stream, but that fetching its metadata (duration and so on) is desirable.
    -   "auto": Hints to the UA that optimistically downloading the entire audio stream is considered desirable.
        Specifying the empty string is equivalent to specifying the value "auto".
-   `controls` = "controls" or "" (empty string) or empty
    Instructs the UA to expose a user interface for controlling playback of the audio stream.
-   `loop` = "loop" or "" (empty string) or empty
    Instructs the UA to seek back to the start of the audio stream upon reaching the end.
-   `mediagroup` = string
    Instructs the UA to link multiple videos and/or audio streams together.
-   `src` = URL potentially surrounded by spaces
    The URL for the audio stream.

## Accessibility

Authors should ensure that the information and user interface components must be presentable to users in ways they can perceive ([WCAG 2.0 - Principle 1: Perceivable](http://www.w3.org/TR/WCAG20/#perceivable)). This includes providing alternatives for time-based media [Guideline 1.2](http://www.w3.org/TR/WCAG20/#media-equiv).

## Formats and Codecs

The specification does not require a specific audio codec to be supported by all user agents. Using both Ogg/Vorbis and MP4/AAC seems to cover most user-agents, however. See the [Audio format support on Wikipedia](http://en.wikipedia.org/wiki/Html5_audio#Audio_format_support).

## Examples

play a mp3 on webpage

``` html
<audio controls src="http://freedownloads.last.fm/download/533190714/she%2Bso%2Bfly.mp3" type="audio/mp3">
</audio>
```

[View live example](http://gist.github.com/7282145)

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/embedded-content.html#the-audio-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/embedded-content-0.html#the-audio-element)
:   W3C Recommendation

## See also

### Other articles

-   [HTML5 and Xiph codecs](http://wiki.xiph.org/Html5)
