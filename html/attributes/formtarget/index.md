---
title: formtarget
tags:
  - Markup
  - Attributes
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Specifies a name or a keyword that indicates where to display the response that is received after submitting the form.'
uri: html/attributes/formtarget

---
# formtarget

## Summary

Specifies a name or a keyword that indicates where to display the response that is received after submitting the form.

Applies to
:   [HTMLInputElement](/html/elements/input)

The formtarget attribute overrides the target attribute of the \<form\> element.

## Examples

``` {.html}
<form action="submit.php">
  Input field: <input type="text" name="inputfield">
  <input type="submit" value="Submit">
  <input type="submit" formtarget="_blank" value="Submit to a new window">
</form>
```

## Related specifications

Specification
:   Status
[HTML5 Forms](http://www.w3.org/TR/html5/forms.html)
:   W3C Recommendation

