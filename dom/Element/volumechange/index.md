---
title: volumechange
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary and compat, also better spec link'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
tags:
  - Events
  - API
  - Audio
  - DOM
  - Video
uri: dom/Element/volumechange

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Overview Table</span>

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
dom/Element

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
</td>
</tr>
</table>
## <span>Examples</span>

The following example implements buttons that change the [**volume**](/dom/HTMLMediaElement/volume) of a video element (v1) by increments of .2 and turn mute on and off. These actions cause the **onvolumechange** event to be raised.

``` html
<button onclick="document.getElementById('v1').volume += 0.2">Volume Up</button>
<button onclick="document.getElementById('v1').volume -= 0.2">Volume Down</button>
<button onclick="document.getElementById('v1').muted = true;">Mute</button>
<button onclick="document.getElementById('v1').muted = false">Unmute</button>
```

## <span>Notes</span>

### <span>Remarks</span>

The [**volume**](/dom/HTMLMediaElement/volume) property of the element represents the current volume level. The default playback volume is `1` (100 percent). The playback volume cannot be increased beyond 100 percent. To invoke this event, do one of the following:

-   Increase or decrease the volume.
-   Mute or unmute the playback.

### <span>Syntax</span>

### <span>Standards information</span>

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.9.12

### <span>Event handler parameters</span>

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## <span>See also</span>

### <span>Related pages (MSDN)</span>

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
