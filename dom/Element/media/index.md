---
title: 'media'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, compat, better spec link'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Element
    href: /dom/Element
standardization_status: 'W3C Candidate Recommendation'
tags:
  - API_Object_Properties
  - API
  - Audio
  - DOM
  - Video
  - Needs_Summary
  - Needs_Examples
uri: dom/Element/media

---
Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var result = element.media;
element.media = value;
```

## Notes

### Remarks

The media property can be used to download different video formats for different sized screens. If the media attribute is omitted, the default value is "all", which means that the media resource is suitable for all media.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.8

## See also

### Related pages

-   source[source](/html/elements/source)
