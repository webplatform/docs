---
title: 'password'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: password
  topic: html
notes:
  - 'Merge Candidate: html/attributes/type. Add example, and more contents.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLInputElement](/dom/HTMLInputElement)'
readiness: 'Not Ready'
summary: 'The password type of the &lt;input&gt; element represents a one-line plain-text edit control for entering a password, which renders input text in such a way as to hide the characters (e.g., a series of asterisks).'
tags:
  - Pages_using_duplicate_arguments_in_template_calls
  - Markup_Elements
  - HTML
  - Needs_Examples
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/msCapsLockWarningOff
uri: html/elements/input/type/password

---
## Summary

The password type of the &lt;input&gt; element represents a one-line plain-text edit control for entering a password, which renders input text in such a way as to hide the characters (e.g., a series of asterisks).

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

## Notes

### Remarks

**Security Warning:  **Using this object incorrectly can compromise the security of your application. Passwords submitted through **input type=password** are not encrypted and therefore not secure. Using Secure Hypertext Transfer Protocol (HTTPS) is strongly recommended. You should also use the **post** method for submitting passwords. This submission method hides the password from most users by placing it in the HTTP header. The **get** method submits the password as part of the URL string, which might be exposed in the **Address** bar and the status bar. You should review the Security Considerations: Dynamic HTML before continuing. **Note**  Starting with Internet Explorer 10, password fields will automatically display a warning if the caps lock is on. To turn off the automatic caps lock warning, use the [**msCapsLockWarningOff**](/w/index.php?title=dom/properties/msCapsLockWarningOff&action=edit&redlink=1) property on the document object.

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.4

### HTML information

{

## Related specifications

[Document Object Model (HTML) Level 1](http://www.w3.org/TR/REC-html40/interact/forms.html#adef-type-INPUT)
:   Recommended

## See also

### Related pages

-   `input`
-   msCapsLockWarningOff[msCapsLockWarningOff](/w/index.php?title=dom/properties/msCapsLockWarningOff&action=edit&redlink=1)
-   Form controls part 1[Form controls part 1](http://go.microsoft.com/fwlink/p/?LinkID=251128)
-   Form controls part 2: validation[Form controls part 2: validation](http://go.microsoft.com/fwlink/p/?LinkID=251131)
