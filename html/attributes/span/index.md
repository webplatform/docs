---
title: 'span'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/span.htm'
compatibility:
  feature: span
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/span

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

This example sets the **SPAN** attribute of the **col** object to two, which causes the **col** to span two columns. The text is right-aligned in these two columns.

``` html
<TABLE BORDER>
<COLGROUP>
<COL SPAN=2 ALIGN=RIGHT>
<COL ALIGN=LEFT>
<TBODY>
<TR>
<TD>This is the first column in the group, and it is
    right-aligned.</TD>
<TD>This is the second column in the group, and it is
    right-aligned.</TD>
<TD>This is the third column in the group, and it is
    left-aligned.</TD>
</TR>
</TABLE>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/span.htm)

## Notes

### Remarks

The **span** property is ignored when set on the **colGroup** element and **colGroup** contains one or more **col** elements. The **span** property provides a more convenient way of grouping columns without having to specify **col** objects.

### Syntax

## See also

### Related pages

-   `col`
-   `colGroup`
