---
title: aria-required
tags:
  - Markup
  - Attributes
  - ARIA
readiness: 'Not Ready'
notes:
  - 'Needs summary, example, spec reference, standardization status'
uri: aria/attributes/aria-required

---
# aria-required

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Applies to
:

**Needs Examples**: This section should include examples.

## Notes

### Remarks

<dl data-table="wikitable">
<dt>
Used in Roles

</dt>
<dd>
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
</dd>
</dl>
  The **aria-required** property indicates which input fields of a form must be filled in before it can be submitted. If the user attempts to submit the form without the required information, you may set [**aria-invalid**](/aria/attributes/aria-invalid) to indicate the error. **Note**  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example `object.setAttribute("aria-valuenow", newValue)`.

### Syntax

### Standards information

-   [Accessible Rich Internet Applications (WAI-ARIA) 1.0](http://go.microsoft.com/fwlink/p/?linkid=203793), Section 6.6

## See also

### Related pages (MSDN)

-   `Accessible Rich Internet Applications (ARIA)`
-   `W3C ARIA-Required`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

