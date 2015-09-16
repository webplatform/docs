---
title: method
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/method

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

When the user enters information in a **form** and clicks the **submit** button, there are two ways the information can be sent from the browser to the server: as part of the URL, or within the body of the HTTP request. The **GET** method appends name/value pairs to the URL. The amount of data that can be sent is limited by the maximum length of a URL, which is 2048 bytes. The URL could be truncated if the form uses a large number of parameters, or if the parameters contain large amounts of data. Parameters passed on the URL are visible in the address field of the browser. This **POST** method packages the name/value pairs inside the body of the HTTP request. When using the **POST** method, there is no theoretical limit to the amount of data that can be sent to the server. Because the parameters are not appended to the URL, this method is slightly more secure.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.3

## See also

### Related pages

-   `form`
-   `action`
