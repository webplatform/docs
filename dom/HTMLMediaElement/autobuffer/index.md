---
title: autobuffer
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLMediaElement
    href: /dom/HTMLMediaElement
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: DOM
  6: Video
uri: dom/HTMLMediaElement/autobuffer

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLMediaElement](/dom/HTMLMediaElement)[dom/HTMLMediaElement](/dom/HTMLMediaElement)

## Syntax

``` js
var result = element.autobuffer;
element.autobuffer = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **autobuffer** method buffers the **audio** or **video** element to prepare for playback. The **autobuffer** attribute indicates that the media element is likely to be used, even though it does not have an [**autoplay**](/dom/HTMLMediaElement/autoplay) attribute. This attribute is ignored if **autoplay** is present. Buffering the media can improve responsiveness when the element is finally played.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)

## See also

### Related pages (MSDN)

-   `media`
-   `audio`
-   `audio`
-   `video element`
-   `video object`
-   `Reference`
-   `autoplay`
-   `preload`
