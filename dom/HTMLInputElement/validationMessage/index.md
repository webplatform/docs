---
title: 'validationMessage'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, compatibility, clean-up of MSDN import to be neutral'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLInputElement
    href: /dom/HTMLInputElement
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/HTMLInputElement
summary: 'Returns the error message that would be displayed if the user submits the form, or an empty string if no error message.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: dom/HTMLInputElement/validationMessage

---
## Summary

Returns the error message that would be displayed if the user submits the form, or an empty string if no error message.

Property of [dom/HTMLInputElement](/dom/HTMLInputElement)[dom/HTMLInputElement](/dom/HTMLInputElement)

## Syntax

**Note**: This property is read-only.

``` js
var validationMessage = inputElement.validationMessage;
```

## Return Value

Returns an object of type StringString

The error message that would be displayed if the user submits the form, or an empty string if no error message.

## Notes

Returns a string containing the standard or custom error message that would be displayed if the user submitted at this time. If no errors are present or the form would validate, an empty string is returned. The following example has a required field, and if the user types "fun" into it, a custom message is set. Try previewing without anything in the field, then enter values, including the word fun: **Note**  For more code samples, see [Form controls part 1](http://go.microsoft.com/fwlink/p/?LinkID=251128) and [Form controls part 2: validation](http://go.microsoft.com/fwlink/p/?LinkID=251131) on the Windows Internet Explorer sample site.

## Related specifications

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## See also

### Related pages

-   HTMLObjectElement[HTMLObjectElement](/dom/HTMLObjectElement)
-   HTMLSelectElement[HTMLSelectElement](/dom/HTMLSelectElement)
-   HTMLInputElement[HTMLInputElement](/dom/HTMLInputElement)
-   HTMLFieldSetElement[HTMLFieldSetElement](/dom/HTMLFieldSetElement)
-   HTMLButtonElement[HTMLButtonElement](/dom/HTMLBGSoundElement)
