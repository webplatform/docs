---
title: date
tags:
  - Markup
  - Elements
  - HTML
readiness: 'Not Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Merge Candidate: html/attributes/type'
summary: 'The date type of the <input> element represents a widget for specifying a date value (year, month, day), with no time zone or time information.'
uri: html/elements/input/type/date

---
# date

## Summary

The date type of the \<input\> element represents a widget for specifying a date value (year, month, day), with no time zone or time information.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

## Examples

``` {.html}
<input type="date" value="2012-12-07">
```

## Notes

On Safari Mobile for iOS, setting [`display`](/css/properties/display)`: block` on an **input** of **type="date"** causes the text within the **input** to become vertically misaligned.

