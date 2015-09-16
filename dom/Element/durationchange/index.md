---
title: 'durationchange'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, compat, better spec link'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
tags:
  - Events
  - API
  - Audio
  - DOM
  - Video
uri: dom/Element/durationchange

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

The following example reads the total duration when the video is loaded and updates the current playback position as the video plays.

``` html
function timeUpdate()
{
    document.getElementById('time').innerHTML = v1.currentTime;
}
function durationChange()
{
    document.getElementById('duration').innerHTML = v1.duration;
}
<video id="v1" controls="true" autoplay="1" src="video.aac"
    ontimeupdate="timeUpdate()" ondurationchange="durationChange()"/>
<div>Time: <span id="time">0</span> of <span id="duration">0</span> seconds.</div>
```

## Notes

### Remarks

Use the [**duration**](/dom/HTMLMediaElement/duration) property to determine the new duration of the clip. This event occurs immediately after [**loadstart**](/dom/Element/loadstart) and before [**loadedmetadata**](/dom/Element/loadedmetadata). To invoke this event, do one of the following:

-   Load a media resource.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.9.12

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## See also

### Related pages

-   audioElement[audioElement](/html/elements/audio)
-   audioApi[audioApi](/apis/audio-video/audio)
-   Document[Document](/dom/Document)
-   source[source](/html/elements/source)
-   videoElement[videoElement](/html/elements/video)
-   videoApi[videoApi](/apis/audio-video/video)
-   Window[Window](/dom/Window)
-   `Reference`
-   loadedmetadata[loadedmetadata](/dom/Element/loadedmetadata)
-   timeupdate[timeupdate](/dom/Element/timeupdate)
