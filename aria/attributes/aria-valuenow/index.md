---
title: aria-valuenow
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - ARIA
uri: aria/attributes/aria-valuenow

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
range

</dt>
</dl>
</td>
</tr>
</table>
  This property applies to elements with an ARIA role of `progressbar`, `slider`, or `spinbutton`. The [**aria-valuemin**](/aria/attributes/aria-valuemin) and [**aria-valuemax**](/aria/attributes/aria-valuemax) properties together specify the allowable range of values, whereas the **aria-valuenow** property specifies the value currently selected. **Note**  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example `object.setAttribute("aria-valuenow", newValue)`.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Accessible Rich Internet Applications (WAI-ARIA) 1.0](http://go.microsoft.com/fwlink/p/?linkid=203793), Section 6.6

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Accessible Rich Internet Applications (ARIA)`
