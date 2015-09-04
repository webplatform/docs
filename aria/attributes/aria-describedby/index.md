---
title: aria-describedby
tags:
  - Markup
  - Attributes
  - ARIA
readiness: 'Not Ready'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Sets or retrieves a list of elements that describe the current object.'
uri: aria/attributes/aria-describedby

---
# aria-describedby

## Summary

Sets or retrieves a list of elements that describe the current object.

Applies to
:

### Syntax

``` {.html}
<element aria-describedby="p" ...>
```

### Property values

Type: String

A space-separated list of id property values.

**Needs Examples**: This section should include examples.

## Notes

This property defines element relationships and associations that cannot be readily determined from the document structure. The **aria-describedby** property is intended to provide additional information which some users might need, and supplements the basic information provided by **label**. If more than one [**id**](/html/attributes/id) property is specified, all elements are combined together to create a single description.

**Note**  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example `object.setAttribute("aria-valuenow", newValue)`.

### Standards information

-   [Accessible Rich Internet Applications (WAI-ARIA) 1.0](http://go.microsoft.com/fwlink/p/?linkid=203793), Section 6.6

## See also

### Related pages

-   `Accessible Rich Internet Applications (ARIA)`
-   `Reference`
-   `aria-controls`
-   `aria-flowto`
-   `aria-labelledby`
-   `aria-owns`
-   `aria-posinset`
-   `aria-setsize`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

