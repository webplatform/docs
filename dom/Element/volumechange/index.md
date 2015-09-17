---
title: 'volumechange'
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
  - Needs_Summary
uri: dom/Element/volumechange

---
## Overview Table

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
## Examples

The following example implements buttons that change the [**volume**](/dom/HTMLMediaElement/volume) of a video element (v1) by increments of .2 and turn mute on and off. These actions cause the **onvolumechange** event to be raised.

``` html
<button onclick="document.getElementById('v1').volume += 0.2">Volume Up</button>
<button onclick="document.getElementById('v1').volume -= 0.2">Volume Down</button>
<button onclick="document.getElementById('v1').muted = true;">Mute</button>
<button onclick="document.getElementById('v1').muted = false">Unmute</button>
```

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

### Related pages

-   audioApi[audioApi](/apis/audio-video/audio)
-   audioElement[audioElement](/html/elements/audio)
-   Document[Document](/dom/Document)
-   source[source](/html/elements/source)
-   videoElement[videoElement](/html/elements/video)
-   videoApi[videoApi](/apis/audio-video/video)
-   Window[Window](/dom/Window)
-   `Reference`
-   volume[volume](/dom/HTMLMediaElement/volume)
-   muted[muted](/dom/HTMLMediaElement/muted)
