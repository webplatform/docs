---
title: canplaythrough
tags:
  - Events
  - API
  - Audio
  - DOM
  - Video
readiness: 'In Progress'
notes:
  - 'summary, examples, clean-up of MSDN import'
summary: 'Fires when enough data is available to determine whether a media is playable at a normal rate without interruptions.'
uri: dom/HTMLMediaElement/canplaythrough

---
# canplaythrough

## Summary

Fires when enough data is available to determine whether a media is playable at a normal rate without interruptions.

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
:    ?

**Needs Examples**: This section should include examples.

## Notes

The **oncanplaythrough** event is raised when data is being fetched at a rate that would allow playback without interruption at the [**defaultPlaybackRate**](/dom/HTMLMediaElement/defaultPlaybackRate). If the [**autoplay**](/dom/HTMLMediaElement/autoplay) attribute is specified, the video starts playing when **oncanplaythrough** is received. This event occurs after [**oncanplay**](/dom/HTMLMediaElement/canplay) and before the first [**onprogress**](/dom/HTMLMediaElement/progress) event is received. To invoke this event, load a media resource.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.9.12

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## Related specifications

Specification
:   Status
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

