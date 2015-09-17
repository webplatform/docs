---
title: 'aria-describedby'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: aria-describedby
  topic: aria
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'Not Ready'
summary: 'Sets or retrieves a list of elements that describe the current object.'
tags:
  - Markup_Attributes
  - ARIA
  - Needs_Examples
uri: aria/attributes/aria-describedby

---
## Summary

Sets or retrieves a list of elements that describe the current object.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
</td>
</tr>
</table>
### Syntax

``` html
<element aria-describedby="p" ...>
```

### Property values

Type: String

A space-separated list of id property values.

## Notes

This property defines element relationships and associations that cannot be readily determined from the document structure. The **aria-describedby** property is intended to provide additional information which some users might need, and supplements the basic information provided by **label**. If more than one [**id**](/html/attributes/id) property is specified, all elements are combined together to create a single description.

**Note**  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example `object.setAttribute("aria-valuenow", newValue)`.

### Standards information

-   [Accessible Rich Internet Applications (WAI-ARIA) 1.0](http://go.microsoft.com/fwlink/p/?linkid=203793), Section 6.6

## See also

### Related pages

-   Accessible Rich Internet Applications (ARIA)[Accessible Rich Internet Applications (ARIA)](/aria)
-   `Reference`
-   aria-controls[aria-controls](/aria/attributes/aria-controls)
-   aria-flowto[aria-flowto](/aria/attributes/aria-flowto)
-   aria-labelledby[aria-labelledby](/aria/attributes/aria-labelledby)
-   aria-owns[aria-owns](/aria/attributes/aria-owns)
-   aria-posinset[aria-posinset](/aria/attributes/aria-posinset)
-   aria-setsize[aria-setsize](/aria/attributes/aria-setsize)
