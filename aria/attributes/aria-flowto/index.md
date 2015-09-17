---
title: 'aria-flowto'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: aria-flowto
  topic: aria
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - ARIA
  - Needs_Summary
  - Needs_Examples
uri: aria/attributes/aria-flowto

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
  This property defines element relationships and associations that cannot be readily determined from the document structure. When the **aria-flowto** property contains a single [**id**](/html/attributes/id) property, the assistive technology should resume reading at the targeted element. However, when the **aria-flowto** property contains multiple **id** properties, the assistive technology should give users the option of navigating to any targeted element. **Note**  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example `object.setAttribute("aria-valuenow", newValue)`.

### Syntax

### Standards information

-   [Accessible Rich Internet Applications (WAI-ARIA) 1.0](http://go.microsoft.com/fwlink/p/?linkid=203793), Section 6.6

## See also

### Related pages

-   Accessible Rich Internet Applications (ARIA)[Accessible Rich Internet Applications (ARIA)](/aria)
-   x-ms-aria-flowfrom[x-ms-aria-flowfrom](/aria/attributes/x-ms-aria-flowfrom)
