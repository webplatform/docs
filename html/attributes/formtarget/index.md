---
title: 'formtarget'
compatibility:
  feature: formtarget
  topic: html
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Specifies a name or a keyword that indicates where to display the response that is received after submitting the form.'
tags:
  - Markup_Attributes
uri: html/attributes/formtarget

---
## Summary

Specifies a name or a keyword that indicates where to display the response that is received after submitting the form.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
[HTMLInputElement](/html/elements/input)

</td>
</tr>
</table>
The formtarget attribute overrides the target attribute of the \<form\> element.

## Examples

``` html
<form action="submit.php">
  Input field: <input type="text" name="inputfield">
  <input type="submit" value="Submit">
  <input type="submit" formtarget="_blank" value="Submit to a new window">
</form>
```

## Related specifications

[HTML5 Forms](http://www.w3.org/TR/html5/forms.html)
:   W3C Recommendation

