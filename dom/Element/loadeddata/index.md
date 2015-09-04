---
title: loadeddata
tags:
  - Events
  - API
  - Audio
  - DOM
  - Video
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Needs summary, example, compat, better spec link'
uri: dom/Element/loadeddata

---
# loadeddata

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

The **onloadeddata** event is raised when data for the immediate current playback position is available. However, it does not guarantee that enough data is available to successfully begin playback. This event occurs after [**loadedmetadata**](/dom/Element/loadedmetadata) and before [**canplay**](/dom/HTMLMediaElement/canplay). To invoke this event, do one of the following:

-   Load a media resource.

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
-   `oncanplay`
-   `oncanplaythrough`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

