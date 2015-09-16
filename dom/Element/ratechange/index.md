---
title: 'ratechange'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary and compat'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
tags:
  - Events
  - API
  - Audio
  - DOM
  - Video
uri: dom/Element/ratechange

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

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

The following example implements buttons that change the playback rate of a video element (v1) by a factor of 0.2. The **Resume** button sets the playback rate back to 1 (100 percent).

``` html
<button onclick="document.getElementById('v1').playbackRate += 0.2">Speed Up</button>
<button onclick="document.getElementById('v1').playbackRate -= 0.2">Slow Down</button>
<button onclick="document.getElementById('v1').playbackRate = 1">Resume</button>
```

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

### Related pages

-   audioApi[audioApi](/apis/audio-video/audio)
-   audioElement[audioElement](/html/elements/audio)
-   Document[Document](/dom/Document)
-   source[source](/html/elements/source)
-   videoElement[videoElement](/html/elements/video)
-   videoApi[videoApi](/apis/audio-video/video)
-   Window[Window](/dom/Window)
-   playbackRate[playbackRate](/dom/HTMLMediaElement/playbackRate)
