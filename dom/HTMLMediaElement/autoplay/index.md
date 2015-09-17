---
title: 'autoplay'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, examples, clean-up of MSDN import'
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
uri: dom/HTMLMediaElement/autoplay

---
Property of [dom/HTMLMediaElement](/dom/HTMLMediaElement)[dom/HTMLMediaElement](/dom/HTMLMediaElement)

## Syntax

``` js
var result = element.autoplay;
element.autoplay = value;
```

## Notes

### Remarks

You can use the **autoplay** attribute rather than script to force the **audio** or **video** to play. The presence of the autoplay attribute, regardless of assigned value, in either the **audio** or **video** element equals true (for example, \<audio autoplay=""\> is true).

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.9.7

## See also

### Related pages

-   media[media](/html/elements/media)
-   `audio`
-   `audio`
-   `video element`
-   `video object`
-   autobuffer[autobuffer](/dom/HTMLMediaElement/autobuffer)
