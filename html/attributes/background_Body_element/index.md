---
title: 'background (Body element)'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: 'background (Body element)'
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Specifies a background image for a document. This attribute is deprecated in HTML4 and not supported in HTML5. Use CSS.'
tags:
  - Markup_Attributes
  - HTML
  - Needs_Examples
uri: 'html/attributes/background (Body element)'

---
## Summary

Specifies a background image for a document. This attribute is deprecated in HTML4 and not supported in HTML5. Use CSS.

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
## Notes

### Remarks

This property is deprecated in favor of the [**background-image**](/css/properties/background-image) attribute of CSS. Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the **background** attribute depends on the context of the reference to the attribute. When read as a Document Object Model (DOM) attribute, **background** returns an absolute URL. The value specified by the page author is returned when **background** is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser. For more information, see Attribute Differences in Internet Explorer 8.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 7.5.1 (Deprecated)

## See also

### Related pages

-   `body`
-   `Reference`
-   backgroundImage[backgroundImage](/css/properties/background-image)
-   `Conceptual`
-   `Defining Document Compatibility`
