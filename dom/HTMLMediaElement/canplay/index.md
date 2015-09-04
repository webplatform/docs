---
title: canplay
tags:
  - Events
  - API
  - Audio
  - DOM
  - Media
  - Video
readiness: 'In Progress'
notes:
  - 'summary, examples, clean-up of MSDN import'
summary: 'Fires whenever enough data is available to determine whether a media is playable.'
uri: dom/HTMLMediaElement/canplay

---
# canplay

## Summary

Fires whenever enough data is available to determine whether a media is playable.

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

The **oncanplay** event is raised when enough data is available to advance the playback position in the direction of playback. This event first occurs after [**onloadeddata**](/dom/Element/loadeddata) and before [**oncanplaythrough**](/dom/HTMLMediaElement/canplaythrough). To invoke this event, load a media resource.

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

