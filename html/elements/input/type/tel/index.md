---
title: 'tel'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: tel
  topic: html
notes:
  - 'Merge Candidate: html/attributes/type'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLInputElement](/dom/HTMLInputElement)'
readiness: 'Not Ready'
summary: 'An input field intended for entering a telephone number; does not enforce any syntax.'
tags:
  - Markup_Elements
  - HTML
uri: html/elements/input/type/tel

---
## Summary

An input field intended for entering a telephone number; does not enforce any syntax.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

## Examples

This example uses the **input type=tel** element to create an empty telephone control. The telephone control does not validate or enforce a specific format, so the **pattern** attribute is used to require the correct format. The **title** attribute gives users a guide when they hover over the field.

``` html
<input type="tel" name="teleNumber" pattern="\(\d\d\d\) ?\d\d\d-\d\d\d\d" title="(###) ###-####"
```

## Notes

### Remarks

**Note**  For code samples, see [Form controls part 1](http://go.microsoft.com/fwlink/p/?LinkID=251128) and [Form controls part 2: validation](http://go.microsoft.com/fwlink/p/?LinkID=251131) on the Windows Internet Explorer sample site.

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.7.1.3

### Members

The **input type=tel** object has these types of members:

-   [\#properties Properties]

#### Properties

The **input type=tel** object has these properties. {

## See also

### Related pages

-   `Reference`
-   `input`
-   pattern[pattern](/html/attributes/pattern)
-   placeholder[placeholder](/html/attributes/placeholder)
