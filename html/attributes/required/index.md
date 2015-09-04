---
title: required
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
summary: 'The required attribute is a boolean attribute. When present, it specifies that an input field must be filled out before submitting the form.'
uri: html/attributes/required

---
# required

## Summary

The required attribute is a boolean attribute. When present, it specifies that an input field must be filled out before submitting the form.

Applies to
:   [HTMLInputElement](/html/elements/input)

## Examples

A required input field

``` {.html}
Username: <input type="text" name="username" required>
```

## Notes

### Remarks

The attribute can be set on text, text area, URL, email, select, checkbox, or radio button elements. It is a Boolean attribute and needs to be specified only on an element. When users hover the mouse over a required field, they’ll see a tool tip stating that it is a required field. The following example shows the validation attribute on a text input field.

## Related specifications

Specification
:   Status
[HTML5](http://www.w3.org/TR/html5/forms.html#the-required-attribute)
:   W3C Recommendation

## See also

### Related pages (MSDN)

-   `HTMLInputElement`
-   `HTMLSelectElement`
-   `HTMLTextAreaElement`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

