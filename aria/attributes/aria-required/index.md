---
title: 'aria-required'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: aria-required
  topic: aria
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - ARIA
  - Needs_Summary
  - Needs_Examples
uri: aria/attributes/aria-required

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

### Syntax

### Standards information

-   [Accessible Rich Internet Applications (WAI-ARIA) 1.0](http://go.microsoft.com/fwlink/p/?linkid=203793), Section 6.6

## See also

### Related pages

-   Accessible Rich Internet Applications (ARIA)[Accessible Rich Internet Applications (ARIA)](/aria)
-   W3C ARIA-Required[W3C ARIA-Required](http://go.microsoft.com/fwlink/p/?linkid=203793)
