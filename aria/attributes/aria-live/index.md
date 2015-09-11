---
title: aria-live
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - ARIA
uri: aria/attributes/aria-live

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
</td>
</tr>
</table>
**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

<table class="wikitable">
<tr>
<th>
Used in Roles

</th>
<td>
<dl>

<dt>
No role required.

</dt>
</dl>
</td>
</tr>
</table>
  The **ariaLive** attribute indicates the priority of updates to a live region. Announcing changes immediately can be disorienting for users. Most updates should be announced only when the user is idle. To supress notifications until after a region has finished updating, set [**ariaBusy**](/aria/attributes/aria-busy). **Note**  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties; for example, `object.setAttribute("aria-valuenow", newValue)`.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Accessible Rich Internet Applications (WAI-ARIA) 1.0](http://go.microsoft.com/fwlink/p/?linkid=203793), Section 6.6

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Accessible Rich Internet Applications (ARIA)`
-   `Reference`
-   `aria-busy`
-   `aria-relevant`
