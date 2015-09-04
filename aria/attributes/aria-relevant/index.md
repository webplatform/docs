---
title: aria-relevant
tags:
  - Markup
  - Attributes
  - ARIA
readiness: 'Not Ready'
notes:
  - 'Needs summary, example, spec reference, standardization status'
uri: aria/attributes/aria-relevant

---
# aria-relevant

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
No role required.

</dt>
</dl>
</dd>
</dl>
  The **ariaRelevant** setting gives a hint about what types of changes are relevant and should be announced by assistive technology. Any change that is not relevant should be treated as if the region had [**ariaLive**](/aria/attributes/aria-live)="off" and should not be announced. The default behavior is equivalent to `additions text`. Updates are announced only as nodes are added, or as text is added or removed. **Note**  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example `object.setAttribute("aria-valuenow", newValue)`.

### Syntax

### Standards information

-   [Accessible Rich Internet Applications (WAI-ARIA) 1.0](http://go.microsoft.com/fwlink/p/?linkid=203793), Section 6.6

## See also

### Related pages (MSDN)

-   `Accessible Rich Internet Applications (ARIA)`
-   `ariaLive`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

