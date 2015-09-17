---
title: 'currentSrc'
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
uri: dom/HTMLMediaElement/currentSrc

---
Property of [dom/HTMLMediaElement](/dom/HTMLMediaElement)[dom/HTMLMediaElement](/dom/HTMLMediaElement)

## Syntax

``` js
var result = element.currentSrc;
element.currentSrc = value;
```

## Notes

### Remarks

-   **currentSrc** returns an empty string if a media resource has not been specified.
-   In some browsers, **currentSrc** will return null if the browser hasn't yet determined which of the sources (if any) it's going to play.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.9.2

## See also

### Related pages

-   media[media](/html/elements/media)
-   `audio`
-   `audio`
-   `video element`
-   `video object`
-   src[src](/dom/HTMLMediaElement/src)
