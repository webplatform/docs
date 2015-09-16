---
title: cellPadding
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Specifies the space, in pixels, between the cell wall and the cell content. Not supported in HTML5. Use CSS.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/cellPadding

---
## Summary

Specifies the space, in pixels, between the cell wall and the cell content. Not supported in HTML5. Use CSS.

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
The *table* element cellpadding attribute is not supported in HTML5. Use CSS instead.

The *cellpadding* attribute specifies the space between each cell stroke. Value has to be a number, and is interpreted as a size in pixels.

Note: Do not confuse this with the *cellspacing* attribute, which specifies the space between cells.

Tip: It may be better to NOT specify a *cellpadding*, and use CSS to apply padding instead.

## Examples

Here is a table where we use the `cellpadding` and `border` table attributes.

``` html
<table border="1" cellpadding="10">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>0</td>
  </tr>
</table>
```

## Related specifications

[Document Object Model (DOM) Level 1, Section 2.5.5](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation

[HTML 4.01 Specification, Section 11.3.3](http://www.w3.org/TR/html401/)
:   Recommendation

## See also

### Related pages

-   [table](/html/elements/table)
-   [cellSpacing](/html/attributes/cells)
