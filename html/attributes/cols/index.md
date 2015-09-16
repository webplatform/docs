---
title: cols
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cols.htm'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/cols

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

This example uses the **COLS** attribute and the **cols** property to set the number of columns in HTML and retrieve the number of columns in script.

``` html
<SCRIPT>
function checkCols(oObject)
{
    var iColumns = oObject.cols;
    alert (iColumns);
}
</SCRIPT>
</HEAD>
<BODY>
<TABLE ID=oTable BORDER COLS=3 onclick="checkCols(this)">
<TR><TD>Column 1</TD><TD>Column 2</TD><TD>Column 3</TD></TR>
</TABLE>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cols.htm)

## Notes

### Remarks

Specifying this number can speed up the processing of the table. Windows Internet Explorer 8 will only render tables up to 1000 columns. To force Windows Internet Explorer 7 rendering mode, see How Do I Take Advantage of the New Features in Internet Explorer 8.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## See also

### Related pages

-   `table`
