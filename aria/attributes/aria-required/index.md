---
title: aria-required
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - ARIA
uri: aria/attributes/aria-required

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
combobox

</dt>
<dt>
gridcell

</dt>
<dt>
listbox

</dt>
<dt>
radiogroup

</dt>
<dt>
spinbutton

</dt>
<dt>
textbox

</dt>
<dt>
tree

</dt>
</dl>
</td>
</tr>
</table>
  The **aria-required** property indicates which input fields of a form must be filled in before it can be submitted. If the user attempts to submit the form without the required information, you may set [**aria-invalid**](/aria/attributes/aria-invalid) to indicate the error. **Note**  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example `object.setAttribute("aria-valuenow", newValue)`.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Accessible Rich Internet Applications (WAI-ARIA) 1.0](http://go.microsoft.com/fwlink/p/?linkid=203793), Section 6.6

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Accessible Rich Internet Applications (ARIA)`
-   `W3C ARIA-Required`
