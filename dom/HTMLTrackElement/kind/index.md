---
title: kind
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: DOM
  6: Video
readiness: 'Not Ready'
notes:
  - 'Summary, examples, compatibility, clean-up of MSDN import'
uri: dom/HTMLTrackElement/kind

---
# kind

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLTrackElement](/dom/HTMLTrackElement)</span></span>

## Syntax

``` {.js}
var result = element.kind;
element.kind = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The keywords can be one of the following:

-   **subtitles** - A transcription or translation of the audio dialog.
-   **captions** - A transcription or translation of the dialog, sound effects, musical cues, or other audio information.
-   **descriptions** - Textual descriptions of the video component, intended for audio synthesis, such as text-to-speech conversion, when the video component is not viewable by the user.
-   **chapters** - Chapter titles to be used for navigating the video content.
-   **metadata** - Information available to be used from script, not displayed in the player or browser.

This property is not implemented for the [**AudioTrack**](/apis/audio-video/AudioTrack) object. **Note**  To create timed text files in both Web Video Text Track (WebVTT) and Timed Text Markup Language (TTML) formats, see [HTML5 Video Caption Maker](http://go.microsoft.com/fwlink/p/?LinkID=251121) on the Windows Internet Explorer test drive site.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)

## See also

### Related pages (MSDN)

-   `track element`
-   `track object`
-   `TextTrack`
-   `AudioTrack`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

