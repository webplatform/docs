---
title: value (input elements)
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: 'html/attributes/value (input elements)'

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
## <span>Examples</span>

This example uses the **input type=text** element to create an empty text control that can contain 15 characters without requiring the user to scroll to read all of the text.

``` html
<INPUT TYPE=text VALUE="" NAME="textbox" SIZE=15>
```

This example uses script to detect the content of the text box and display it in a dialog box.

``` html
<SCRIPT>
function detectEntry()
{
    alert("Your name is " + textbox.value)
}
</SCRIPT>
```

## <span>Notes</span>

### <span>Remarks</span>

The purpose of the **value** property depends on the type of control as described in the following table. {

### <span>Syntax</span>

### <span>Standards information</span>

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.4

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `input`
-   `input type=checkbox`
-   `input type=password`
-   `input type=text`
-   `input type=file`
-   `input type=hidden`
-   `input type=button`
-   `input type=radio`
-   `input type=reset`
-   `input type=submit`
-   `input type=range`
-   `input type=number`
-   `input type=email`
-   `input type=url`
-   `input type=tel`
