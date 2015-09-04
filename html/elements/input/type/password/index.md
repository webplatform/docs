---
title: password
tags:
  - Pages
  - using
  - duplicate
  - arguments
  - in
  - template
  - calls
  - Markup
  - Elements
  - HTML
readiness: 'Not Ready'
notes:
  - 'Merge Candidate: html/attributes/type. Add example, and more contents.'
summary: 'The password type of the <input> element represents a one-line plain-text edit control for entering a password, which renders input text in such a way as to hide the characters (e.g., a series of asterisks).'
uri: html/elements/input/type/password
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/msCapsLockWarningOff

---
# password

## Summary

The password type of the \<input\> element represents a one-line plain-text edit control for entering a password, which renders input text in such a way as to hide the characters (e.g., a series of asterisks).

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

**Needs Examples**: This section should include examples.

## Notes

### Remarks

**Security Warning:  **Using this object incorrectly can compromise the security of your application. Passwords submitted through **input type=password** are not encrypted and therefore not secure. Using Secure Hypertext Transfer Protocol (HTTPS) is strongly recommended. You should also use the **post** method for submitting passwords. This submission method hides the password from most users by placing it in the HTTP header. The **get** method submits the password as part of the URL string, which might be exposed in the **Address** bar and the status bar. You should review the Security Considerations: Dynamic HTML before continuing. **Note**  Starting with Internet Explorer 10, password fields will automatically display a warning if the caps lock is on. To turn off the automatic caps lock warning, use the [**msCapsLockWarningOff**](/w/index.php?title=dom/properties/msCapsLockWarningOff&action=edit&redlink=1) property on the document object.

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.4

### HTML information

{

## Related specifications

Specification
:   Status
[Document Object Model (HTML) Level 1](http://www.w3.org/TR/REC-html40/interact/forms.html#adef-type-INPUT)
:   Recommended

## See also

### Related pages (MSDN)

-   `input`
-   `msCapsLockWarningOff`
-   `Form controls part 1`
-   `Form controls part 2: validation`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

