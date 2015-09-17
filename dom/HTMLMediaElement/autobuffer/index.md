---
title: 'autobuffer'
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
  - API_Object_Properties
  - API
  - Audio
  - DOM
  - Video
  - Needs_Summary
  - Needs_Examples
uri: dom/HTMLMediaElement/autobuffer

---
Property of [dom/HTMLMediaElement](/dom/HTMLMediaElement)[dom/HTMLMediaElement](/dom/HTMLMediaElement)

## Syntax

``` js
var result = element.autobuffer;
element.autobuffer = value;
```

## Notes

### Remarks

The **autobuffer** method buffers the **audio** or **video** element to prepare for playback. The **autobuffer** attribute indicates that the media element is likely to be used, even though it does not have an [**autoplay**](/dom/HTMLMediaElement/autoplay) attribute. This attribute is ignored if **autoplay** is present. Buffering the media can improve responsiveness when the element is finally played.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)

## See also

### Related pages

-   media[media](/html/elements/media)
-   `audio`
-   `audio`
-   `video element`
-   `video object`
-   `Reference`
-   autoplay[autoplay](/dom/HTMLMediaElement/autoplay)
-   preload[preload](/dom/HTMLMediaElement/preload)
