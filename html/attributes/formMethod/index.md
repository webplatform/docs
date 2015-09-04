---
title: formMethod
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
summary: 'The formmethod attribute defines the HTTP method for sending form-data to the action URL.'
uri: html/attributes/formMethod

---
# formMethod

## Summary

The formmethod attribute defines the HTTP method for sending form-data to the action URL.

Applies to
:   [HTMLInputElement](/html/elements/input)

The formmethod attribute overrides the method attribute of the \<form\> element.

## Examples

``` {.html}
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

### Related pages (MSDN)

-   `HTMLInputElement`
-   `HTMLButtonElement`
-   `input type=submit`
-   `formEnctype`
-   `formAction`
-   `formNoValidate`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

