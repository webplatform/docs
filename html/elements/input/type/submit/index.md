---
title: 'submit'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: submit
  topic: html
notes:
  - 'Merge Candidate: html/attributes/type. Add example.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLInputElement](/dom/HTMLInputElement)'
readiness: 'Not Ready'
summary: 'An input form button that submits the form data to the server.'
tags:
  - Pages_using_duplicate_arguments_in_template_calls
  - Markup_Elements
  - HTML
  - Needs_Examples
uri: html/elements/input/type/submit

---
## Summary

An input form button that submits the form data to the server.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

## Notes

### Remarks

Use the [**VALUE**](/html/attributes/value_(button_element)) attribute to create a button with a display label that cannot be edited by the user. The default label is `Submit Query`. If the user clicks the **Submit** button to submit the form, and that button has a [**name**](/html/attributes/name) attribute specified, that button contributes a name/value pair to the submitted data. If the **INPUT type=submit** element is part of a **FORM** element, it appears as a button with a dark border, which indicates the user can press ENTER to submit the form. When there is more than one **INPUT type=submit** in the same form, pressing enter submits the form using the first **INPUT type=submit**, unless another **INPUT type=submit** has focus. When another **INPUT type=submit** has focus, pressing enter submits the form using that **INPUT type=submit**.

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.4
-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.7.1.19

### HTML information

{

## See also

### Related pages

-   `Reference`
-   `button`
-   `input`
