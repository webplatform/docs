---
title: 'formMethod'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: formMethod
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The formmethod attribute defines the HTTP method for sending form-data to the action URL.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/formMethod

---
## Summary

The formmethod attribute defines the HTTP method for sending form-data to the action URL.

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
The formmethod attribute overrides the method attribute of the \<form\> element.

## Examples

``` html
<form action="submit_post.php" method="post">
  Input field: <input type="text" name="inputfield">
  <input type="submit" value="Submit">
  <input type="submit" formmethod="get" formaction="submit_get.asp" value="Submit using GET">
</form>
```

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.19.6

## See also

### Related pages

-   HTMLInputElement[HTMLInputElement](/dom/HTMLInputElement)
-   HTMLButtonElement[HTMLButtonElement](/dom/HTMLBGSoundElement)
-   `input type=submit`
-   formEnctype[formEnctype](/html/attributes/formEnctype)
-   formAction[formAction](/html/attributes/formAction)
-   formNoValidate[formNoValidate](/html/attributes/formNoValidate)
