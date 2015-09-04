---
title: validationMessage
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'examples, compatibility, clean-up of MSDN import to be neutral'
summary: 'Returns the error message that would be displayed if the user submits the form, or an empty string if no error message.'
uri: dom/HTMLInputElement/validationMessage

---
# validationMessage

## Summary

Returns the error message that would be displayed if the user submits the form, or an empty string if no error message.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLInputElement](/dom/HTMLInputElement)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var validationMessage = inputElement.validationMessage;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The error message that would be displayed if the user submits the form, or an empty string if no error message.

**Needs Examples**: This section should include examples.

## Notes

Returns a string containing the standard or custom error message that would be displayed if the user submitted at this time. If no errors are present or the form would validate, an empty string is returned. The following example has a required field, and if the user types "fun" into it, a custom message is set. Try previewing without anything in the field, then enter values, including the word fun: **Note**  For more code samples, see [Form controls part 1](http://go.microsoft.com/fwlink/p/?LinkID=251128) and [Form controls part 2: validation](http://go.microsoft.com/fwlink/p/?LinkID=251131) on the Windows Internet Explorer sample site.

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## See also

### Related pages (MSDN)

-   `HTMLObjectElement`
-   `HTMLSelectElement`
-   `HTMLInputElement`
-   `HTMLFieldSetElement`
-   `HTMLButtonElement`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

