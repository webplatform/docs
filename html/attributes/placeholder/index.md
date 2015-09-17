---
title: 'placeholder'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: placeholder
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The placeholder attribute specifies a short hint that describes the expected value of an input field (e.g. a sample value or a short description of the expected format).'
tags:
  - Markup_Attributes
  - HTML
uri: html/attributes/placeholder

---
## Summary

The placeholder attribute specifies a short hint that describes the expected value of an input field (e.g. a sample value or a short description of the expected format).

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
The short hint is displayed in the input field before the user enters a value.

## Examples

``` html
Address: <input type="text" name="address" placeholder="Insert here your address" />
Date of birth: <input type="text" name="day" placeholder="DD" />
<input type="text" name="month" placeholder="MM" />
<input type="text" name="year" placeholder="YYYY" />
```

## Notes

### Remarks

The **placeholder** attribute can be used on text or text area input controls, or with text-based input attributes **URL** or **email**. The following example shows the placeholder text on a URL input field.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.7.3.12

## See also

### Related pages

-   HTMLInputElement[HTMLInputElement](/dom/HTMLInputElement)
-   HTMLTextAreaElement[HTMLTextAreaElement](/dom/HTMLTextAreaElement)
