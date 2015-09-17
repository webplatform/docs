---
title: 'formAction'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: formAction
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The formaction attribute specifies the URL of a file that will process the input control when the form is submitted.'
tags:
  - Markup_Attributes
  - HTML
uri: html/attributes/formAction

---
## Summary

The formaction attribute specifies the URL of a file that will process the input control when the form is submitted.

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
The formaction attribute overrides the action attribute of the \<form\> element.

## Examples

``` html
<form action="login.php">
  First name: <input type="text" name="name"><br>
  Last name: <input type="text" name="surname"><br>
  <input type="submit" value="Login"><br>
  <input type="submit" formaction="admin_login.php"
  value="Login as admin">
</form>
```

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.19.6

## See also

### Related pages

-   HTMLInputElement[HTMLInputElement](/dom/HTMLInputElement)
-   HTMLButtonElement[HTMLButtonElement](/dom/HTMLBGSoundElement)
-   `input type=image`
-   formMethod[formMethod](/html/attributes/formMethod)
-   formEnctype[formEnctype](/html/attributes/formEnctype)
-   formNoValidate[formNoValidate](/html/attributes/formNoValidate)
