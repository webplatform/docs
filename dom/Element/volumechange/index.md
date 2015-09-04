---
title: volumechange
tags:
  - Events
  - API
  - Audio
  - DOM
  - Video
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Needs summary and compat, also better spec link'
uri: dom/Element/volumechange

---
# volumechange

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

The following example implements buttons that change the [**volume**](/dom/HTMLMediaElement/volume) of a video element (v1) by increments of .2 and turn mute on and off. These actions cause the **onvolumechange** event to be raised.

    <button onclick="document.getElementById('v1').volume += 0.2">Volume Up</button>
    <button onclick="document.getElementById('v1').volume -= 0.2">Volume Down</button>
    <button onclick="document.getElementById('v1').muted = true;">Mute</button>
    <button onclick="document.getElementById('v1').muted = false">Unmute</button>

## Notes

### Remarks

The [**volume**](/dom/HTMLMediaElement/volume) property of the element represents the current volume level. The default playback volume is `1` (100 percent). The playback volume cannot be increased beyond 100 percent. To invoke this event, do one of the following:

-   Increase or decrease the volume.
-   Mute or unmute the playback.

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
-   `volume`
-   `muted`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

