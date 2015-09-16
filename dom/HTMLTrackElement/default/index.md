---
title: default
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Summary, examples, compatibility, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLTrackElement
    href: /dom/HTMLTrackElement
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: DOM
  6: Video
uri: dom/HTMLTrackElement/default

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLTrackElement](/dom/HTMLTrackElement)[dom/HTMLTrackElement](/dom/HTMLTrackElement)

## Syntax

``` js
var result = element.default;
element.default = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

This property defines whether the [**TextTrack**](/apis/audio-video/TextTrack) is the default for a given **video** element. The presence of the default attribute, regardless of assigned value, in the track element equals true. If no default is specified, no text track will be displayed with the video. Any track can be selected using the default attribute. If more than one track has the default attribute, the first track with the attribute will be default, and the others will be ignored. **Note**  To create timed text files in both Web Video Text Track (WebVTT) and Timed Text Markup Language (TTML) formats, see [HTML5 Video Caption Maker](http://go.microsoft.com/fwlink/p/?LinkID=251121) on the Windows Internet Explorer test drive site.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)

## See also

### Related pages

-   `track element`
-   `track object`
