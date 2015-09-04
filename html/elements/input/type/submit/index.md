---
title: submit
tags:
  - Pages
  - using
  - duplicate
  - arguments
  - in
  - template
  - calls
  - Markup
  - Elements
  - HTML
readiness: 'Not Ready'
notes:
  - 'Merge Candidate: html/attributes/type. Add example.'
summary: 'An input form button that submits the form data to the server.'
uri: html/elements/input/type/submit

---
# submit

## Summary

An input form button that submits the form data to the server.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Use the [**VALUE**](/html/attributes/value_(button_element)) attribute to create a button with a display label that cannot be edited by the user. The default label is `Submit Query`. If the user clicks the **Submit** button to submit the form, and that button has a [**name**](/html/attributes/name) attribute specified, that button contributes a name/value pair to the submitted data. If the **INPUT type=submit** element is part of a **FORM** element, it appears as a button with a dark border, which indicates the user can press ENTER to submit the form. When there is more than one **INPUT type=submit** in the same form, pressing enter submits the form using the first **INPUT type=submit**, unless another **INPUT type=submit** has focus. When another **INPUT type=submit** has focus, pressing enter submits the form using that **INPUT type=submit**.

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.4
-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.7.1.19

### HTML information

{

## See also

### Related pages (MSDN)

-   `Reference`
-   `button`
-   `input`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

