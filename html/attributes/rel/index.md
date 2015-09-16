---
title: rel
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Describes the relationship from the current document to the anchor specified by the href attribute.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/rel

---
## Summary

Describes the relationship from the current document to the anchor specified by the href attribute.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
<http://docs.webplatform.org/wiki/html/elements/a>

</td>
</tr>
</table>
**Needs Examples**: This section should include examples.

## Notes

### Remarks

If no values are indicated, the **rel** property's default relationship is an empty string. This property is used only when the [**href**](/css/cssom/properties/href) property is applied. The **Offline**, **Search**, **Shortcut Icon**, and **Stylesheet** values apply only to the **link** object. The **rel** property is similar to the [**rev**](/html/attributes/rev) property, but the semantics of these two properties' link types are in the reverse direction. For example, a link from A to B with REL="X" expresses the same relationship as a link from B to A with REV="X". An anchor can have both **rel** and **rev** properties. Internet Explorer 8 and later. In IE8 Standards mode, the **rel** content attribute locates the **Alternate** token regardless of its position in a space-delimited list of tokens. For example, **rel** will locate **Alternate** whether it is parsed as **rel="alternate stylesheet"** or **rel="stylesheet alternate"**. For more information on IE8 mode, see Defining Document Compatibility. The **Offline** value is available in Microsoft Internet Explorer 5 and later. For more information about CDF files and offline favorites, see Enhancing Offline Favorites. CDF is obsolete as of Internet Explorer 7.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 12.2

## See also

### Related pages

-   `a`
-   `link`
-   `Reference`
-   `rev`
-   `Other Resources`
-   `Subscribing to Content with Web Slices`
