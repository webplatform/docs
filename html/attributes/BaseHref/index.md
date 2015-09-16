---
title: BaseHref
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'deletion candidate - old, not xUserAgent'
readiness: 'Not Ready'
summary: 'Retrieves a string of the URL where the object tag can be found, often the href of the document that the object is in, or the value set by a base element.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/BaseHref

---
## Summary

Retrieves a string of the URL where the object tag can be found, often the href of the document that the object is in, or the value set by a base element.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
**Needs Examples**: This section should include examples.

## Notes

### Remarks

Use the **BaseHref** property to resolve relative paths when locating an **object**. The following rules determine the resulting *p*.

-   If the **object** element is on a page containing a **base** element, then *p* takes the value of the **base**.[**href**](/html/attributes/href_(base)) property.
-   If the **object** element is on a page with `javascript` or `vbscript`, or is about **protocol** URLs, then *p* takes the value of the current page's parent page URL. This applies to **object**.**BaseHref** property requests in **iframe**/ **frame** elements as well.
-   For all other **object** elements, *p* takes the value of the page they are found on.

### Syntax

## See also

### Related pages

-   `object`
