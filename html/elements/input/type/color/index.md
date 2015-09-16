---
title: color
notes:
  - 'Merge Candidate: html/attributes/type'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLInputElement](/dom/HTMLInputElement)'
readiness: 'Not Ready'
standardization_status: 'W3C Working Draft'
summary: 'The color type of the &lt;input&gt; element provides a widget for selecting a color value.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/input/type/color

---
## Summary

The color type of the &lt;input&gt; element provides a widget for selecting a color value.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

## Examples

When viewed using a supporting user agent, the following example shows a field, usually indicating a red color. When clicked, a color picker shows up. Selecting a color would change the indicated color to the chosen color.

``` html
<input type="color" value="#ff0000"/>
```

## Usage

     Use this input type to let the user choose a color using a standard color picker.

## Notes

-   Currently, most user agents do not implement this input type. A customized implementation or poly-fill can usually provide a close alternative.
-   The value can only express opaque colors, there is no support for an alpha channel/transparency.
