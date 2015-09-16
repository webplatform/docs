---
title: date
notes:
  - 'Merge Candidate: html/attributes/type'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLInputElement](/dom/HTMLInputElement)'
readiness: 'Not Ready'
standardization_status: 'W3C Working Draft'
summary: 'The date type of the &lt;input&gt; element represents a widget for specifying a date value (year, month, day), with no time zone or time information.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/input/type/date

---
## Summary

The date type of the &lt;input&gt; element represents a widget for specifying a date value (year, month, day), with no time zone or time information.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

## Examples

``` html
<input type="date" value="2012-12-07">
```

## Notes

On Safari Mobile for iOS, setting [`display`](/css/properties/display)`: block` on an **input** of **type="date"** causes the text within the **input** to become vertically misaligned.
