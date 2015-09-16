---
title: noWrap
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/noWrap

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

Care should be taken when the **noWrap** property is used in conjunction with the [**width**](/html/attributes/width_(img,_input_elements)) attribute of [**table**](/html/elements/table) or **td** elements. Wordwrap still occurs in a **td** element that has its [**WIDTH**](/html/attributes/width_(img,_input_elements)) attribute set to a value smaller than the unwrapped content of the cell, even if the **noWrap** property is set to true. Therefore, the **WIDTH** attribute takes precedence over the **noWrap** property in this scenario. If a **td** element has its **noWrap** set to true and the [**WIDTH**](/html/attributes/width_(img,_input_elements)) attribute of its [**table**](/html/elements/table) element is set to a smaller dimension than the rendered content of the **td** element, wordwrap does not occur. In this case, the **noWrap** setting takes precedence over the **WIDTH** attribute.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 11.2.6 (Deprecated)

## See also

### Related pages

-   `body`
-   `dd`
-   `div`
-   `dt`
-   `td`
-   `th`
