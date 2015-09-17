---
title: 'aria-live'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: aria-live
  topic: aria
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - ARIA
  - Needs_Summary
  - Needs_Examples
uri: aria/attributes/aria-live

---
<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
</td>
</tr>
</table>
## Notes

### Remarks

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

### Syntax

### Standards information

-   [Accessible Rich Internet Applications (WAI-ARIA) 1.0](http://go.microsoft.com/fwlink/p/?linkid=203793), Section 6.6

## See also

### Related pages

-   Accessible Rich Internet Applications (ARIA)[Accessible Rich Internet Applications (ARIA)](/aria)
-   `Reference`
-   aria-busy[aria-busy](/aria/attributes/aria-busy)
-   aria-relevant[aria-relevant](/aria/attributes/aria-relevant)
