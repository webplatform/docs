---
title: 'scheme'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: scheme
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/scheme

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

In the following two examples, the value of **scheme** defines how to interpret the value of the "date" property.

``` html
//Here scheme="Europe" implies "DD-MM-YYYY"
<META scheme="Europe" name="date" content="05-04-1962">
```

[
    <code>//Here scheme{{=}}"USA" implies "MM-DD-YYYY"<META scheme{{=}}"USA" name{{=}}"date" content{{=}}"04-05-1962"></code>

View live example]

The following example of the **meta** shows how the **scheme** can be used to clarify the value of the "id" property.

``` html
<META scheme="customer" name="id" content="Fancy Pants">
```

## Notes

### Remarks

**scheme** was introduced in Microsoft Internet Explorer 6 The **scheme** property can provide a context to correctly interpret otherwise ambiguous data formats such as those for date and time. It can also be used to identify the object's content itself. There is no functionality implemented for this property unless defined by the author.

### Syntax

## See also

### Related pages

-   `meta`
