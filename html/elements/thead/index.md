---
title: thead
tags:
  - Markup
  - Elements
  - HTML
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
notes:
  - 'Should have automatic child links generated.'
summary: 'The thead element  (<thead>) identifies header rows at the top of a table, usually containing column labels.  It may contain one or more rows of <th> or <td> cells.'
uri: html/elements/thead

---
# thead

## Summary

The thead element (\<thead\>) identifies header rows at the top of a table, usually containing column labels. It may contain one or more rows of \<th\> or \<td\> cells.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLTableSectionElement](/dom/HTMLTableSectionElement)

## Examples

The following code example uses the *thead'* element and the [**table**](/html/elements/table), [**tbody**](/html/elements/tbody), [**td**](/html/elements/td), and [**tr**](/html/elements/tr) elements to create a table that includes the first row in the table header and the second row in the table body.

``` {.html}
<table>
<thead>
  <tr>
    <th scope="col">Player</th>
    <th scope="col">Position</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>James, Lebron</td>
    <td>SF</td>
  </tr>
  <tr>
    <td>Wade, Dwayne</td>
    <td>SG</td>
  </tr>
  <tr>
    <td>Bosh, Chris</td>
    <td>PF</td>
  </tr>
</tbody>
</table>
```

## Notes

### Remarks

Valid tags within the **THEAD** element include:

-   **td** \* chances are should be a th not a td, and scope of column
-   **th**
-   **tr**

You can specify only one **thead** object specified for any given [**table**](/html/elements/table) object. The [**table**](/html/elements/table) object and its associated elements have a separate table object model, which uses different methods than the general object model.

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 11.2.3

Â

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/tabular-data.html#the-thead-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/tabular-data.html#the-thead-element)
:   W3C Recommendation
[HTML 4.01](http://www.w3.org/TR/html401/struct/tables.html#edef-THEAD)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

