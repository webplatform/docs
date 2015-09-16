---
title: pattern
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The pattern attribute specifies a regular expression that the &lt;input&gt; element''s value is checked against.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/pattern

---
## Summary

The pattern attribute specifies a regular expression that the &lt;input&gt; element's value is checked against.

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
## Examples

``` html
Numeric field: <input type="text" name="numericField" pattern="[0-9]*" />
Country code: <input type="text" name="country_code" pattern="[A-Za-z]{3}" title="Three letter country code">
```

## Notes

### Remarks

Several generic messages are displayed for a variety of validation errors. If you use a title attribute on an input element, it will both be shown as alt text for the field, as well as be appended to the generic error message. The following example shows a ZIP code number format.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.7.3.9

## See also

### Related pages

-   `HTMLInputElement`
