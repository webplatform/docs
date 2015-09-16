---
title: 'vcard name'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: 'vcard name'
  topic: html
notes:
  - 'Deletion Candidate'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: 'html/attributes/vcard name'

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
## Examples

This example uses the **VCARD\_NAME** attribute to map the value of the text field to the e-mail address specified by the Profile Assistant.

``` html
<INPUT
TYPE = text NAME= "CustomerEmail"
VCARD_NAME = "vCard.Email"
>
```

## Notes

### Remarks

A vCard is a standards-based way to refer to common personal information about a user. When a **VCARD\_NAME** attribute is specified, the AutoComplete box is populated with mapped values from the Profile Assistant and any other submitted values stored for that domain. For example, if a user enters an e-mail address into a text field that exposes a **VCARD\_NAME** attribute set to `vCard.Email`, AutoComplete suggests any e-mail information provided in the Profile Assistant. If the user submits a different e-mail address, the new information becomes available on that domain for other text fields with the same **VCARD\_NAME** value. If the **VCARD\_NAME** attribute is not specified, the name of the text field is used to map the submitted information. However, information from the Profile Assistant is not used. You can disable the AutoComplete feature by specifying `no` to the [**AUTOCOMPLETE**](/html/attributes/autocomplete) attribute. Even though you can map **PASSWORD** values for AutoComplete, the ability to store this information can be disabled. When this occurs, the user is prompted for a confirmation before storing the value. The object model and the document do not have access to information provided by the AutoComplete feature until the user selects one of the suggestions for the text field. This property is not supported in HTML Applications.

### Syntax

### Standards information

There are no standards that apply here.

## See also

### Related pages

-   `input type=password`
-   `input type=text`
-   `Using AutoComplete in HTML Forms`
