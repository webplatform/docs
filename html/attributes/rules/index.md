---
title: rules
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rules.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/table_rules_border.htm'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/rules

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
## <span>Examples</span>

This example initially sets the **RULES** attribute on the table, and then uses the **rules** property to dynamically change the table borders.

``` html
<TABLE ID="oID_1" RULES="cols">
<THEAD>
<TR>
<TD>EST</TD><TD>1am</TD><TD>8pm</TD>
</TR>
</THEAD>
<TR>
<TD>CST</TD><TD>2am</TD><TD>9pm</TD>
</TR>
<TR>
<TD>MST</TD><TD>3am</TD><TD>10pm</TD>
</TR>
<TFOOT>
<TR>
<TD>PST</TD><TD>4am</TD><TD>11pm</TD>
</TR>
</TFOOT>
</TABLE>
<P>
<BUTTON onclick="oID_1.rules=''">No borders</BUTTON>
<BUTTON onclick="oID_1.rules='none'">Exterior border</BUTTON>
<BUTTON onclick="oID_1.rules='all'">All borders</BUTTON><BR>
<BUTTON onclick="oID_1.rules='cols'">Column borders</BUTTON>
<BUTTON onclick="oID_1.rules='groups'">Groups borders</BUTTON>
<BUTTON onclick="oID_1.rules='rows'">Table row borders</BUTTON>
</P>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rules.htm)

In this example, the table object contains the **RULES** attribute set to `cols` and the [**border**](/css/properties/border) attribute set to an empty string (""). This example demonstrates that if the **RULES** attribute is set to an empty string (""), the **border** attribute will cause the table to show all borders, trumping the **RULES** attribute.

``` html
<TABLE ID="oID_1" BORDER="" RULES="cols">
<THEAD>
<TR>
<TD>EST</TD><TD>1am</TD><TD>8pm</TD>
</TR>
</THEAD>
<TR>
<TD>CST</TD><TD>2am</TD><TD>9pm</TD>
</TR>
<TR>
<TD>MST</TD><TD>3am</TD><TD>10pm</TD>
</TR>
<TFOOT>
<TR>
<TD>PST</TD><TD>4am</TD><TD>11pm</TD>
</TR>
</TFOOT>
</TABLE>
<P>
<BUTTON onclick="oID_1.rules=''">No borders</BUTTON>
<BUTTON onclick="oID_1.rules='none'">Exterior border</BUTTON>
<BUTTON onclick="oID_1.rules='all'">All borders</BUTTON><BR>
<BUTTON onclick="oID_1.rules='cols'">Column borders</BUTTON>
<BUTTON onclick="oID_1.rules='groups'">Groups borders</BUTTON>
<BUTTON onclick="oID_1.rules='rows'">Table row borders</BUTTON>
</P>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/table_rules_border.htm)

## <span>Notes</span>

### <span>Remarks</span>

The value **none** turns off only the interior borders. To turn off the table borders, set the **rules** property to , or omit the **RULES** attribute from the [**table**](/html/elements/table) object.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `table`
-   `frame`
