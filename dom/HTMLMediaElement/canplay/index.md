---
title: canplay
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, examples, clean-up of MSDN import'
readiness: 'In Progress'
summary: 'Fires whenever enough data is available to determine whether a media is playable.'
tags:
  - Events
  - API
  - Audio
  - DOM
  - Media
  - Video
uri: dom/HTMLMediaElement/canplay

---
## <span>Summary</span>

Fires whenever enough data is available to determine whether a media is playable.

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

The **oncanplay** event is raised when enough data is available to advance the playback position in the direction of playback. This event first occurs after [**onloadeddata**](/dom/Element/loadeddata) and before [**oncanplaythrough**](/dom/HTMLMediaElement/canplaythrough). To invoke this event, load a media resource.

## <span>Related specifications</span>

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
