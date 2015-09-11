---
title: disabled
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/7282815'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Prevents users from changing, clicking on, or submitting an element.'
tags:
  - Markup
  - Attributes
  - HTML
  - JavaScript
  - Security
uri: html/attributes/disabled

---
## <span>Summary</span>

Prevents users from changing, clicking on, or submitting an element.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
[html/elements/input](/html/elements/input)

</td>
</tr>
</table>
When an element has the disabled attribute set, it appears dimmed and does not respond to user input. Disabled elements do not respond to mouse events or the [contentEditable](/html/attributes/contentEditable) property.

If an element is contained within a disabled ([fieldset](/html/elements/fieldset), the fieldset will override its disabled attribute.

The disabled attribute will prevent javascript click events on the element.

If the disabled element is present without a value (`<input disabled>`) it will default to true. Other valid values are `true` and `false`.

### <span>Affects</span>

When this is present a user cannot make the element active. Further, when the form is submitted, the input's name and value will not be present. If you wish to submit the value, but make it so the user cannot manipulate the value see the [readonly attribute](/html/attributes/readonly).

## <span>Examples</span>

This shows a basic form, with an email input and a submit button disabled.

``` html
<!doctype html>
<title>Disabled attribute demo</title>
<form role="form">
    <label for="name">Name</label>
    <input name="name">
    <br>
    <label for="email">Email</label>
    <input type="email" name="email" disabled>
    <br>
    <input type="submit" disabled>
    <input type="button" value="cancel">
</form>
```

[View live example](http://code.webplatform.org/gist/7282815)

