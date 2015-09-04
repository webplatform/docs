---
title: emptied
tags:
  - Events
  - API
  - Audio
  - DOM
  - Video
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Needs summary, examples, compat, better spec link'
uri: dom/Element/emptied

---
# emptied

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

Synchronous
:   No
Bubbles
:   No
Target
:   dom/Element
Cancelable
:   No
Default action
:

**Needs Examples**: This section should include examples.

## Notes

### Remarks

When the [**load**](/dom/HTMLMediaElement/load) method is called, the media element stops any previously running media and resets the element. Playback restarts immediately if the [**autoplay**](/dom/HTMLMediaElement/autoplay) attribute is specified. To invoke this event, do the following:

-   Call the media element's [**load**](/dom/HTMLMediaElement/load) method.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.9.12

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## See also

### Related pages (MSDN)

-   `audioApi`
-   `audioElement`
-   `Document`
-   `source`
-   `videoElement`
-   `videoApi`
-   `Window`
-   `Reference`
-   `load`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

