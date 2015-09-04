---
title: aria-hidden
tags:
  - Markup
  - Attributes
  - ARIA
readiness: 'Not Ready'
notes:
  - 'Needs summary, spec reference, standardization status'
uri: aria/attributes/aria-hidden

---
# aria-hidden

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Applies to
:

## Examples

You can use a CSS rule to show or hide the element based on the value of the **aria-hidden** state, as shown here:

``` {.css}
[aria-hidden=true] {visibility: hidden;}
```

## Notes

### Remarks

<dl data-table="wikitable">
<dt>
Used in Roles

</dt>
<dd>
<dl>

<dt>
No role required.

</dt>
</dl>
</dd>
</dl>
  This **ariaHidden** state indicates whether an element is visible or hidden. **Note**  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example `object.setAttribute("aria-valuenow", newValue)`.

### Syntax

### Standards information

-   [Accessible Rich Internet Applications (WAI-ARIA) 1.0](http://go.microsoft.com/fwlink/p/?linkid=203793), Section 6.6

## See also

### Related pages (MSDN)

-   `Accessible Rich Internet Applications (ARIA)`
-   `W3C ARIA-Hidden`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

