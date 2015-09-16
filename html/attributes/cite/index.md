---
title: cite
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/cite

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

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
## Examples

The example shows the use of the **cite** property.

``` html
<HTML>
<BODY>
<Q id="greatQuote" cite="http://www.Shakespeare.the.great.com">
To Be or Not to Be, That is the Question.</Q>
</BODY>
</HTML>
```

## Notes

### Remarks

This property is designed to contain a Uniform Resource Identifier (URI) that points to information about why a document was changed, or about the source of a quotation. There is no functionality implemented for this property unless defined by the author. Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the **cite** attribute for the **del**, **ins**, and **q** elements depends on the context of the reference to the attribute. When read as a Document Object Model (DOM) attribute, **cite** returns an absolute URL. The value specified by the page author is returned when **cite** is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser. For more information, see Attribute Differences in Internet Explorer 8. **cite** was introduced in Microsoft Internet Explorer 6. The value of the **cite** attribute for the **del**, **ins**, and **q** elements depends on the context of the reference to the attribute. When read as a DOM attribute, **cite** returns an absolute URL. The value specified by the document author is returned when **cite** is read as a content attribute, when the document is displayed in an earlier document compatibility mode.

### Syntax

## See also

### Related pages

-   `blockQuote`
-   `q`
-   `ins`
-   `del`
