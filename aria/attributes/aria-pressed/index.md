---
title: 'aria-pressed'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: aria-pressed
  topic: aria
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - ARIA
uri: aria/attributes/aria-pressed

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
button

</dt>
</dl>
</td>
</tr>
</table>
  Buttons with a defined **aria-pressed** state can be toggled. (When **aria-pressed** is **true** the button is down, when **false** it is up.) Simple command buttons do not need to define a **aria-pressed** state. **Note**  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example `object.setAttribute("aria-valuenow", newValue)`.

### Syntax

### Standards information

-   [Accessible Rich Internet Applications (WAI-ARIA) 1.0](http://go.microsoft.com/fwlink/p/?linkid=203793), Section 6.6

## See also

### Related pages

-   Accessible Rich Internet Applications (ARIA)[Accessible Rich Internet Applications (ARIA)](/aria)
-   W3C ARIA-Pressed[W3C ARIA-Pressed](http://go.microsoft.com/fwlink/p/?linkid=203793)
