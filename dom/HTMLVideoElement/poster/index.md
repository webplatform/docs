---
title: 'poster'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, compatibility, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLVideoElement
    href: /dom/HTMLVideoElement
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/HTMLVideoElement
summary: 'Valid URL to an image ressource that will be displayed until the first frame of the video is available or will be displayed if no valid video ressource is available at all.'
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: DOM
  6: Video
uri: dom/HTMLVideoElement/poster

---
## Summary

Valid URL to an image ressource that will be displayed until the first frame of the video is available or will be displayed if no valid video ressource is available at all.

Property of [dom/HTMLVideoElement](/dom/HTMLVideoElement)[dom/HTMLVideoElement](/dom/HTMLVideoElement)

## Syntax

``` js
var result = element.poster;
element.poster = value;
```

## Return Value

Returns an object of type StringString

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The poster property requires a non-empty URL.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.6

## See also

### Related pages

-   `video element`
-   `video object`
