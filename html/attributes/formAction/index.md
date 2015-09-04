---
title: formAction
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
summary: 'The formaction attribute specifies the URL of a file that will process the input control when the form is submitted.'
uri: html/attributes/formAction

---
# formAction

## Summary

The formaction attribute specifies the URL of a file that will process the input control when the form is submitted.

Applies to
:   [HTMLInputElement](/html/elements/input)

The formaction attribute overrides the action attribute of the \<form\> element.

## Examples

``` {.html}
<form action="login.php">
  First name: <input type="text" name="name">
  Last name: <input type="text" name="surname">
  <input type="submit" value="Login">
  <input type="submit" formaction="admin_login.php"
  value="Login as admin">
</form>
```

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.19.6

## See also

### Related pages (MSDN)

-   `HTMLInputElement`
-   `HTMLButtonElement`
-   `input type=image`
-   `formMethod`
-   `formEnctype`
-   `formNoValidate`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

