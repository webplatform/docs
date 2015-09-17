---
title: 'content'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: content
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - HTML
  - Needs_Summary
uri: html/attributes/content

---
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
Internationalization topics related to the `content` element:

-   [Choosing and applying a character encoding](http://www.w3.org/International/techniques/authoring-html#choosing)
-   [Changing to UTF-8](http://www.w3.org/International/techniques/authoring-html#changing)
-   [Declaring the character encoding for HTML](http://www.w3.org/International/techniques/authoring-html#indoc)

## Examples

This example causes the browser to reload the document every two seconds.

``` html
<meta http-equiv="refresh" content="2">
```

This example sets the character set for the document.

``` html
<meta http-equiv="Content-Type"

      content="text/html; charset=utf-8">
```

This example disables theme support for the document.

``` html
<meta http-equiv="msthemecompatible" content="no">
```

This example tells Internet Explorer to display a document in IE9 mode, if possible.

``` html
<meta http-equiv="X-UA-Compatible" content="IE=9">
```

## Notes

### Remarks

Developers using the [**httpEquiv**](/html/attributes/httpEquiv) and **content** attributes to refresh documents from alternate URLs should treat the value of **content** as untrusted data. For more information, please see Security Considerations: Dynamic HTML.

As of Internet Explorer 8, the [**httpEquiv**](/html/attributes/httpEquiv) attribute also supports a value of `x-ua-compatible`, which allows developers to specify the document compatibility mode that Internet Explorer should use to display a webpage. To do this, set the **content** attribute to a **String** value containing a comma-delimited list of one or more of the following values.

{

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 7.4.4

## See also

### Related pages

-   `Reference`
-   httpEquiv[httpEquiv](/html/attributes/httpEquiv)
-   `meta`
-   `Conceptual`
-   `Defining Document Compatibility`
