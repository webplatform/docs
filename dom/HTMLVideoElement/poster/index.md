---
title: poster
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
## <span>Summary</span>

Valid URL to an image ressource that will be displayed until the first frame of the video is available or will be displayed if no valid video ressource is available at all.

Property of [dom/HTMLVideoElement](/dom/HTMLVideoElement)[dom/HTMLVideoElement](/dom/HTMLVideoElement)

## <span>Syntax</span>

``` js
var result = element.poster;
element.poster = value;
```

## <span>Return Value</span>

Returns an object of type StringString

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

The poster property requires a non-empty URL.

### <span>Syntax</span>

### <span>Standards information</span>

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.6

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `video element`
-   `video object`
