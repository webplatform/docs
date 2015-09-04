---
title: aria-activedescendant
tags:
  - Markup
  - Attributes
  - ARIA
readiness: 'Not Ready'
notes:
  - 'Needs summary, example, spec reference, standardization status'
uri: aria/attributes/aria-activedescendant
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/events/keypress

---
# aria-activedescendant

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
composite

</dt>
<dt>
group

</dt>
<dt>
textbox

</dt>
</dl>
</dd>
</dl>
  To simplify keyboard navigation, an element that gains focus may specify the currently active child element by [**id**](/html/attributes/id).

The container element should change the designated descendant during a [**keypress**](/w/index.php?title=dom/events/keypress&action=edit&redlink=1) event. The container should also ensure that the current child has a style that visibly shows it is active, such as an outline or different background color. **Note**  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example `object.setAttribute("aria-valuenow", newValue)`.

### Syntax

### Standards information

-   [Accessible Rich Internet Applications (WAI-ARIA) 1.0](http://go.microsoft.com/fwlink/p/?linkid=203793), Section 6.6

## See also

### Related pages (MSDN)

-   `Accessible Rich Internet Applications (ARIA)`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

