---
title: cuechange
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, compat, and better spec link'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
tags:
  - Events
  - API
  - Audio
  - DOM
  - Video
uri: dom/Element/cuechange

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
 ?

</td>
</tr>
</table>
**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

In the following example, when a cuechange event is received on the track element, the [**activeCue**](/apis/audio-video/TextTrack/activeCues) is displayed as an HTML nodes that replace the **span** element. **Note**  To create timed text files in both Web Video Text Track (WebVTT) and Timed Text Markup Language (TTML) formats, see [HTML5 Video Caption Maker](http://go.microsoft.com/fwlink/p/?LinkID=251121) on the Windows Internet Explorer test drive site.

### <span>Syntax</span>

### <span>Standards information</span>

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)

### <span>Event handler parameters</span>

*handler* [in]
:   Type: **Function**Handler function to process the oncuechange event.

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `HTMLElement`
-   `TextTrack`
-   `HTMLTrackElement`
