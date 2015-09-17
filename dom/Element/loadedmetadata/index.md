---
title: 'loadedmetadata'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, compat and better spec link'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
tags:
  - Events
  - API
  - Audio
  - DOM
  - Video
  - Needs_Summary
  - Needs_Examples
uri: dom/Element/loadedmetadata

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
## Notes

### Remarks

The **onloadedmetadata** event is raised when enough of the resource has been obtained to know the full duration of the resource. In the case of a **video** element, the dimensions of the video are also known. This event occurs after [**ondurationchange**](/dom/Element/durationchange). To invoke this event, do one of the following:

-   Load a media resource.

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
-   onloadstart[onloadstart](/dom/Element/loadstart)
-   onloadeddata[onloadeddata](/dom/Element/loadeddata)
