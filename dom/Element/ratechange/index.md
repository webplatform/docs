---
title: ratechange
tags:
  - Events
  - API
  - Audio
  - DOM
  - Video
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Needs summary and compat'
uri: dom/Element/ratechange

---
# ratechange

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

## Examples

The following example implements buttons that change the playback rate of a video element (v1) by a factor of 0.2. The **Resume** button sets the playback rate back to 1 (100 percent).

    <button onclick="document.getElementById('v1').playbackRate += 0.2">Speed Up</button>
    <button onclick="document.getElementById('v1').playbackRate -= 0.2">Slow Down</button>
    <button onclick="document.getElementById('v1').playbackRate = 1">Resume</button>

## Notes

### Remarks

This event is raised when the value of [**playbackRate**](/dom/HTMLMediaElement/playbackRate) changes. The playback rate can be increased to a maximum of `2` (200 percent), or decreased to `0`. To invoke this event, do one of the following:

-   Increase or decrease the value of **playbackRate**.

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
-   `playbackRate`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

