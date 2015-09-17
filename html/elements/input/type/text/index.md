---
title: 'text'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: text
  topic: html
notes:
  - 'Merge Candidate: html/attributes/type'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLInputElement](/dom/HTMLInputElement)'
readiness: 'Not Ready'
summary: 'The input element with a type attribute whose value is &quot;text&quot; represents a one-line plain text edit control for the input element’s value.'
tags:
  - Pages_using_duplicate_arguments_in_template_calls
  - Markup_Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/spellcheck
uri: html/elements/input/type/text

---
## Summary

The input element with a type attribute whose value is &quot;text&quot; represents a one-line plain text edit control for the input element’s value.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

## Examples

This example uses the **INPUT type=text** element to create an empty text control that can contain 15 characters without requiring the user to scroll to read all of the text.

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

## Notes

### Remarks

The [**SIZE**](/html/attributes/size_(control)) attribute sets the number of visible characters in the **INPUT type=text** element. The [**MAXLENGTH**](/html/attributes/maxLength) attribute sets the maximum number of characters that can be entered. **Security Warning:  **Using this object incorrectly can compromise the security of your application. When submitting text through **INPUT type=text** over an intranet or the Internet, validating the text string is recommended. For instance, you might validate the string for a restricted set of known, good values (such as letters and numbers) and ignore the rest. You should review the Security Considerations: Dynamic HTML before continuing. **Note**  For more code samples, see [Form controls part 1](http://go.microsoft.com/fwlink/p/?LinkID=251128) and [Form controls part 2: validation](http://go.microsoft.com/fwlink/p/?LinkID=251131) on the Windows Internet Explorer sample site.

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.4

### HTML information

{

## See also

### External resources

<http://www.w3.org/TR/html-markup/input.text.html#input.text>

### Related pages

-   `Reference`
-   spellcheck[spellcheck](/w/index.php?title=dom/properties/spellcheck&action=edit&redlink=1)
-   `input`
-   `textArea`
