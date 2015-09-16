---
title: 'emptied'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, compat, better spec link'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
tags:
  - Events
  - API
  - Audio
  - DOM
  - Video
uri: dom/Element/emptied

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
**Needs Examples**: This section should include examples.

## Notes

### Remarks

When the [**load**](/dom/HTMLMediaElement/load) method is called, the media element stops any previously running media and resets the element. Playback restarts immediately if the [**autoplay**](/dom/HTMLMediaElement/autoplay) attribute is specified. To invoke this event, do the following:

-   Call the media element's [**load**](/dom/HTMLMediaElement/load) method.

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
-   load[load](/dom/HTMLMediaElement/load)
