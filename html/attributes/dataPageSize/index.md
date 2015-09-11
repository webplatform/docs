---
title: dataPageSize
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/firstPage
    - dom/methods/lastPage
    - dom/methods/previousPage
uri: html/attributes/dataPageSize

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

In this example, a text box is bound to the customer\_name field supplied by a data source object with an ID of customer. Because the text box is located within a data-bound [**table**](/html/elements/table), the text box is repeated to display each of the records in the data source. The **DATAPAGESIZE** attribute on the **table** limits the display to 10 records.

``` html
<table datasrc="#customer" datapagesize=10>
   <tr><td><input type=texbox datafld="customer_name"></td></tr>
</table>
```

## <span>Notes</span>

### <span>Remarks</span>

The [**firstPage**](/w/index.php?title=dom/methods/firstPage&action=edit&redlink=1) and [**lastPage**](/w/index.php?title=dom/methods/lastPage&action=edit&redlink=1) methods are used to navigate directly to the first and last pages of a databound table, respectively. The **nextPage** and [**previousPage**](/w/index.php?title=dom/methods/previousPage&action=edit&redlink=1) methods are used to navigate sequentially through the pages of a databound table.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `table`
-   `Reference`
-   `firstPage`
-   `lastPage`
-   `nextPage`
-   `previousPage`
-   `Conceptual`
-   `Introduction to Data Binding`
