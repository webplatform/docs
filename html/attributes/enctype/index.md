---
title: enctype
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/enctype

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
**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **ENCTYPE** attribute of the form specifies how the HTTP request should be encoded. All GET requests are submitted as **application/x-www-form-urlencoded**. The value of **multipart/form-data** is required (with a POST request) to submit a file to the server. The value of **text/plain** forces the request to be POST. Windows Internet Explorer 8 and later. In IE8 Standards mode, the **enctype** Document Object Model (DOM) attribute is now supported and reflects the **ENCTYPE** content attribute. For more information, see Attribute Differences in Internet Explorer 8. The **enctype** property was introduced in Internet Explorer 8. If backward compatibility is required, use the [**encoding**](/html/attributes/encoding) property.

### Syntax

## See also

### Related pages (MSDN)

-   `form`
-   `encoding`
