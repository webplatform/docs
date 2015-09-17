---
title: 'aria-relevant'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: aria-relevant
  topic: aria
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - ARIA
  - Needs_Summary
  - Needs_Examples
uri: aria/attributes/aria-relevant

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
  The **ariaRelevant** setting gives a hint about what types of changes are relevant and should be announced by assistive technology. Any change that is not relevant should be treated as if the region had [**ariaLive**](/aria/attributes/aria-live)="off" and should not be announced. The default behavior is equivalent to `additions text`. Updates are announced only as nodes are added, or as text is added or removed. **Note**  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example `object.setAttribute("aria-valuenow", newValue)`.

### Syntax

### Standards information

-   [Accessible Rich Internet Applications (WAI-ARIA) 1.0](http://go.microsoft.com/fwlink/p/?linkid=203793), Section 6.6

## See also

### Related pages

-   Accessible Rich Internet Applications (ARIA)[Accessible Rich Internet Applications (ARIA)](/aria)
-   ariaLive[ariaLive](/aria/attributes/aria-live)
