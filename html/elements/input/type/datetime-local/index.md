---
title: datetime-local
notes:
  - 'Merge Candidate: html/attributes/type'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLInputElement](/dom/HTMLInputElement)'
readiness: 'Not Ready'
standardization_status: 'W3C Working Draft'
summary: 'The datetime-local type of the &lt;input&gt; element represents a widget for setting a date-time value (year, month, day, hours, minutes, seconds, milliseconds) with no time zone information.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/input/type/datetime-local

---
## Summary

The datetime-local type of the &lt;input&gt; element represents a widget for setting a date-time value (year, month, day, hours, minutes, seconds, milliseconds) with no time zone information.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

## Examples

``` html
<input type="datetime-local" value="2012-12-14T19:00">
```

## Notes

On Safari Mobile for iOS, setting [`display`](/css/properties/display)`: block` on an **input** of **type="datetime-local"** causes the text within the **input** to become vertically misaligned.
